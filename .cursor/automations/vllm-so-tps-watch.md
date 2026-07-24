# Manual paste draft — vLLM SO TPS upstream watch

Use this if Save fails or the Automations form is empty.

## Fields to fill in the Automations UI

- **Name:** vLLM SO TPS upstream watch
- **Description:** Daily vLLM #49013 watch; update watch md; Slack DM
- **Trigger:** Scheduled → Custom cron → `0 12 * * *` (confirm timezone = KST / Asia/Seoul)
- **Repository:** Single repo → `JejuWayfarer/check-vllm-issue` · branch `main`
- **Tools:** Send to Slack → channel/DM `D0BDN5V2TDE`
- **Memories:** on (default OK)

## Instructions (prompt) — paste as-is

매일 정오(KST)에 이 레포(main)에서 실행한다.

1) GitHub API로 vllm-project/vllm 이슈 #49013, PR #49150, PR #49168 상태(open/closed/merged) 확인
2) vllm main의 apply_grammar_bitmask staging이 여전히 torch.full 인지 확인
3) 관련 신규 이슈/PR 검색: apply_grammar_bitmask, #45424, structured-output throughput/perf, grammar bitmask staging. MTP+SO 인접(#49210 등)은 참고. 코어 3개 제외한 신규만 기록
4) 루트 파일 vllm-so-tps-watch.md 에 행 추가(없으면 생성). 컬럼: 확인시각(KST), #49013, #49150, #49168, main staging, 관련 신규, 비고
5) 변경을 커밋한다. main 직접 푸시가 되면 main에 푸시하고, 안 되면 PR을 연다
6) Slack DM으로 한국어 요약 전송: 코어 상태 + 관련 신규 유무. 해결 시( #49013 closed AND (픽 머지 또는 staging 제거) ) RESOLVED 명시

감시 로그 외 다른 파일은 바꾸지 말 것.

## Before Save checklist

1. Cursor Settings → Integrations: **GitHub** connected, Cloud Agents enabled for `JejuWayfarer/check-vllm-issue`
2. **Slack** connected to Cursor; open a DM with the Cursor bot once if needed
3. Repository is selected (cron defaults to *no repo* — must set single repo)
4. Slack tool points at `D0BDN5V2TDE`
