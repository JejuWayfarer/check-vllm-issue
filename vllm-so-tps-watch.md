# vLLM SO TPS upstream watch

> **Superseded:** daily updates moved to [`vllm-so-tps-watch-v2.md`](./vllm-so-tps-watch-v2.md). This file is frozen.

OCR extract decode TPS 회귀 (v0.23→0.24, guided JSON + MTP) — `apply_grammar_bitmask` staging (#45424 → #49013).

**해결 판정:** `#49013` closed **그리고** (#49150 또는 #49168 머지, 또는 main에서 `torch.full` staging 제거)

| 확인 시각 (KST) | #49013 | #49150 | #49168 | main staging | 관련 신규 (코어 외) | 비고 |
|-----------------|--------|--------|--------|--------------|---------------------|------|
| 2026-08-04 12:00 | open | open | closed | 여전히 `torch.full` | #50924 [open] [Bug]: EngineCore dies on first guided-decoding request when dspark sp; #49981 [open] [Bug]: tool_choice: "required" causes xgrammar FSM crash / infinite ha; #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s | 서버 cron 갱신 |
| 2026-08-03 12:00 | open | open | closed | 여전히 `torch.full` | #49981 [open] [Bug]: tool_choice: "required" causes xgrammar FSM crash / infinite ha; #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative  | 서버 cron 갱신 |
| 2026-08-02 12:00 | open | open | closed | 여전히 `torch.full` | #49981 [open] [Bug]: tool_choice: "required" causes xgrammar FSM crash / infinite ha; #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative  | 서버 cron 갱신 |
| 2026-08-01 12:00 | open | open | closed | 여전히 `torch.full` | #49981 [open] [Bug]: tool_choice: "required" causes xgrammar FSM crash / infinite ha; #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative  | 서버 cron 갱신 |
| 2026-07-31 12:00 | open | open | open | 여전히 `torch.full` | #49981 [open] [Bug]: tool_choice: "required" causes xgrammar FSM crash / infinite ha; #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative  | 서버 cron 갱신 |
| 2026-07-30 12:00 | open | open | open | 여전히 `torch.full` | #49981 [open] [Bug]: tool_choice: "required" causes xgrammar FSM crash / infinite ha; #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative  | 서버 cron 갱신 |
| 2026-07-29 12:00 | open | open | open | 여전히 `torch.full` | #49981 [open] [Bug]: tool_choice: "required" causes xgrammar FSM crash / infinite ha; #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative  | 서버 cron 갱신 |
| 2026-07-28 12:00 | open | open | open | 여전히 `torch.full` | #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative ; #48765 [open] [Bug]: disable_any_whitespace is silently ignored at the request level | 서버 cron 갱신 |
| 2026-07-27 12:00 | open | open | open | 여전히 `torch.full` | #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative ; #48765 [open] [Bug]: disable_any_whitespace is silently ignored at the request level | 서버 cron 갱신 |
| 2026-07-26 12:00 | open | open | open | 여전히 `torch.full` | #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative ; #48765 [open] [Bug]: disable_any_whitespace is silently ignored at the request level | 서버 cron 갱신 |
| 2026-07-25 12:00 | open | open | open | 여전히 `torch.full` | #49694 [open] [Bug]: ngram_gpu spec decode + structured outputs (xgrammar) + async s; #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative ; #48765 [open] [Bug]: disable_any_whitespace is silently ignored at the request level | 서버 cron 갱신 |
| 2026-07-24 12:00 | open | open | open | 여전히 `torch.full` | #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative ; #48765 [open] [Bug]: disable_any_whitespace is silently ignored at the request level; #48663 [open] [Bug]: `minimax_m3` reasoning parser splits structured-output JSON at  | 서버 cron 갱신 |
| 2026-07-24 11:23 | open | open | open | 여전히 `torch.full` | #49210 [open] [Bug]: Engine core livelock (100% CPU, no crash) with MTP speculative ; #48765 [open] [Bug]: disable_any_whitespace is silently ignored at the request level; #48663 [open] [Bug]: `minimax_m3` reasoning parser splits structured-output JSON at  | 서버 cron 갱신 |
| 2026-07-24 11:00 | open | open | open | 여전히 `torch.full` | **#49210** open (MTP+xgrammar SO livelock, 0.24 회귀) — C1과 동일 원인 아님. SO bitmask staging 주제 추가 신규 없음 | 수동 갱신 (오늘 기준) |

## 링크

- https://github.com/vllm-project/vllm/issues/49013
- https://github.com/vllm-project/vllm/pull/49150
- https://github.com/vllm-project/vllm/pull/49168
- https://github.com/vllm-project/vllm/issues/49210
- 회귀 도입: https://github.com/vllm-project/vllm/pull/45424
