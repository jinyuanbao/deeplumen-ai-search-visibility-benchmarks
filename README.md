---
pretty_name: DeepLumen AI Search Visibility Benchmarks
language:
  - en
tags:
  - ai-search
  - ecommerce
  - benchmarks
  - agentic-commerce
  - search-visibility
task_categories:
  - tabular-classification
  - question-answering
license: cc-by-4.0
size_categories:
  - n<1K
---

# DeepLumen AI Search Visibility Benchmarks

Clean, source-linked benchmark data derived from public [DeepLumen](https://www.deeplumen.com/)
case study pages. The dataset is intended as a publish-ready starter package for GitHub and
Hugging Face, with each metric tied back to an editorially relevant canonical source.

## Dataset Files

- `data/ai_search_visibility_benchmarks.json` and `.csv`: one row per public case study.
- `data/metric_observations.json` and `.csv`: one row per measured benchmark observation.
- `data/timeline_events.json` and `.csv`: implementation and outcome milestones.
- `data/sources.csv`: source URLs and provenance notes.
- `docs/schema.md`: field definitions and release notes.

## Intended Use

This dataset can support public benchmarking, AI search visibility analysis, retrieval demos,
and examples for evaluating agentic search performance across ecommerce categories.

## Source Links

The dataset uses public DeepLumen pages as source material. Key canonical references include:

- [Qbedding home and living case](https://www.deeplumen.com/industries/home-living/)
- [Nullport electronics case](https://www.deeplumen.com/industries/electronics/)
- [Vermille health and beauty case](https://www.deeplumen.com/industries/health-beauty/)
- [Atelier Vauclair fashion and apparel case](https://www.deeplumen.com/industries/fashion-apparel/)
- [Magarri AI citations case study](https://www.deeplumen.com/blog/magarri-case-study/)
- [Looktech AI citations case study](https://www.deeplumen.com/blog/looktech-case-study/)
- [1988 Coffee Estate AI search case study](https://www.deeplumen.com/blog/1988-coffee-estate-case-study/)
- [ACCC scoring system](https://www.deeplumen.com/blog/accc-scoring-system/)

## Data Sensitivity

All rows are derived from public pages on [www.deeplumen.com](https://www.deeplumen.com/).
Brand names are retained only where already publicly published by DeepLumen. The
`brand_public_alias` field can be replaced with anonymous IDs such as `brand_001` before release
if a more conservative publication mode is preferred.

## Citation

If you use this dataset, cite [DeepLumen](https://www.deeplumen.com/) and link to the
corresponding source URL in each row.

## License

This dataset is released under `CC-BY-4.0`.
