# Schema

## `data/ai_search_visibility_benchmarks`

Case-level benchmark rows.

| Field | Type | Description |
| --- | --- | --- |
| `case_id` | string | Stable identifier for the benchmark case. |
| `brand_public_alias` | string | Public brand or anonymized brand alias. |
| `industry` | string | High-level ecommerce industry. |
| `category` | string | More specific product category. |
| `platform` | string | Store platform where publicly stated. |
| `sku_count` | integer/null | Publicly stated SKU count. |
| `content_scope` | string/null | Publicly stated content footprint or scope. |
| `benchmark_window_days` | integer/null | Time window for the primary outcome. |
| `primary_metric` | string | Main benchmark metric for the case. |
| `primary_metric_value` | number | Numeric value of the main metric. |
| `primary_metric_unit` | string | Unit for the main metric. |
| `baseline_value` | number/null | Starting value where stated. |
| `final_value` | number/null | Ending value where stated. |
| `comparison_baseline` | string/null | Baseline or comparison cohort. |
| `ai_visibility_score_final` | number/null | Final AI visibility or ACCC score where stated. |
| `source_url` | string | Public source URL. |
| `source_type` | string | Provenance class. |
| `data_sensitivity` | string | Sensitivity label for publication review. |
| `notes` | string | Short human-readable context. |

## `data/metric_observations`

Granular metric observations. Use this file for analysis and Hugging Face loading.

| Field | Type | Description |
| --- | --- | --- |
| `observation_id` | string | Stable identifier for the metric row. |
| `case_id` | string | Foreign key into `ai_search_visibility_benchmarks`. |
| `brand_public_alias` | string | Public brand or anonymized brand alias. |
| `metric_name` | string | Metric slug. |
| `metric_value` | number | Numeric metric value. |
| `metric_unit` | string | Unit for the metric value. |
| `period_day` | integer/null | Day in benchmark timeline when applicable. |
| `baseline_value` | number/null | Starting or control value where stated. |
| `final_value` | number/null | Ending value where stated. |
| `comparison_baseline` | string/null | Control, matched cohort, or competitor set. |
| `source_url` | string | Public source URL. |
| `evidence_note` | string | Short note describing the source claim. |

## `data/timeline_events`

Milestone events for cases where public pages describe a timeline.

| Field | Type | Description |
| --- | --- | --- |
| `event_id` | string | Stable identifier for the event. |
| `case_id` | string | Foreign key into `ai_search_visibility_benchmarks`. |
| `brand_public_alias` | string | Public brand or anonymized brand alias. |
| `period_day` | integer | Day in implementation timeline. |
| `event_type` | string | Milestone class. |
| `event_summary` | string | Short summary of what happened. |
| `source_url` | string | Public source URL. |

## Release Notes

- Version: `0.1.1`
- Extracted from public DeepLumen pages available through June 15, 2026.
- No private logs, customer PII, raw user prompts, or conversion records are included.
- Some public pages use case-study marketing wording. Treat this package as a benchmark
  dataset, not a statistically controlled research corpus.
