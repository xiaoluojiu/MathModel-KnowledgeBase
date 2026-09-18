# CUMCM 2022–2023 A/B Evidence Extraction Index v1

> Scope: A/B only. This index records verified official paper-display sources and the extraction queue. It deliberately separates source evidence from inferred model patterns.

## 2023 official paper-display corpus

The Ministry of Education's China University Student Online lists three A papers and three B papers for 2023:

### A
- A0165
- A0127
- A092

### B
- B477
- B311
- B226

Source: official 2023 paper-display index: https://dxs.moe.gov.cn/zx/hd/sxjm/sxjmlw/2023qgdxssxjmjslwzs/2023gjsbqgdxssxjmjslwzs.shtml

Individual A-paper pages are image-page publications rather than ordinary HTML full text, so model claims must be extracted from page images/OCR before being marked `method_verified`.

## 2022 official paper-display corpus

The official 2022 index lists three A papers and three B papers:

### A
- A001
- A022
- A171

### B
- B030
- B035
- B086

Source: official 2022 paper-display index: https://dxs.moe.gov.cn/zx/hd/sxjm/sxjmlw/2022qgdxssxjmjslwzs/2022gjsbqgdxssxjmjslwzs.shtml

## Evidence labels

- `official_indexed`: paper is listed by the official competition-related publication portal.
- `page_verified`: relevant paper page/image was inspected.
- `method_verified`: a model/method is supported by visible paper正文/公式/algorithm text.
- `pattern_inferred`: a reusable problem/data pattern inferred from verified evidence; not a claim that the paper explicitly named that pattern.
- `historical_usage`: only for methods directly evidenced in the paper.

## Extraction fields

For each paper extract:

1. problem/subproblem
2. variables and data type
3. assumptions
4. mathematical structure
5. model/method and role
6. parameter estimation
7. solver/algorithm
8. validation/error analysis
9. sensitivity/robustness
10. limitations
11. alternative methods appearing in the paper
12. reusable problem pattern
13. model tags and relation edges

## Quality rule

A paper's use of a method is historical evidence, not a recommendation. Recommendation requires matching the new problem's objective, data pattern, constraints, assumptions, and computational requirements against the Model Card.

## Next extraction order

1. 2023 A0165/A0127/A092
2. 2023 B477/B311/B226
3. 2022 A001/A022/A171
4. 2022 B030/B035/B086
5. reconcile extracted methods with existing Model Cards and negative-match rules
