# vLLM SO TPS upstream watch v2

OCR extract decode TPS 회귀 (v0.23→0.24) — structured-output path (#45424 → #49013).

**RESOLVED:** `#49150` 또는 `#49780` 또는 `#49919` 중 **하나 이상 `merged`** (`#49013` closed / `torch.full` 제거는 게이트 아님).

**Abandoned:** [#49168](https://github.com/vllm-project/vllm/pull/49168) closed without merge (staging cache; maintainers preferred #49919).

## Links

- https://github.com/vllm-project/vllm/issues/49013
- https://github.com/vllm-project/vllm/pull/49150
- https://github.com/vllm-project/vllm/pull/49780
- https://github.com/vllm-project/vllm/pull/49919
- Frozen v1 log: `vllm-so-tps-watch.md`

| 확인 시각 (KST) | #49013 | #49150 | #49780 | #49919 | torch.full (참고) | 관련 신규 | 비고 |
|-----------------|--------|--------|--------|--------|------------------|-----------|------|
| 2026-08-04 12:53 | open | open | open | open | 있음 | #50924 [open] [Bug]: EngineCore dies on first guided-decoding request when dspark sp | 서버 cron 갱신 |
| 2026-08-04 12:53 | open | open | open | open | 있음 | #50924 [open] [Bug]: EngineCore dies on first guided-decoding request when dspark sp; #49738 [open] [Bugfix][Structured Output][Spec Decode] Fix async grammar bitmask ali | 서버 cron 갱신 |
