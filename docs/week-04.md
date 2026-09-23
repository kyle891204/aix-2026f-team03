# 4주차 활동지 / Week 4 Worksheet

**주제 선택과 요구 명세 / Choosing a problem & writing the spec**

- 작성일 / Date: 260923
- 참여자 / Present: 강수연, 김용태, 송선우, 이재림

---

## ① 주제 선택 / Choosing one problem

| 항목 Item | 내용 |
|---|---|
| 선택한 주제 Chosen | 외국인 유학생을 위한 맞춤형 학사/생활 통합 플랫폼 |
| 선택 근거 Why | 유학생에게 부족한 것은 정보의 양이 아니라, "이 정보가 나에게 해당하는지, 그래서 지금 무엇을 해야 하는지"를 알려주는 안내이다. 비자, 입국, 수강신청 등 필수 정보는 여러 곳에 흩어져있고, 번역기로는 구체적인 처리 순서나 맥락을 파악하기 어려워 행정적 불이익과 불안감을 얻기 쉽다. 또한 일상에서도 언어, 문화적 차이와 내국인 중심 커뮤니티에서의 정보 단절로 인해 고립되기 쉬우며, 실제로 학업스트레스와 낯선 환경에서의 적응 부족으로 인해 유학생의 심각한 우울증이나 극단적 선택으로 이어지는 등 심리적 위기가 큰 상황이다. 이에 복잡한 학교 공지를 맞춤형 행동 정보로 변환해 학업 및 행정 부담을 덜고, 유학생들이 다국어로 검증된 생활 정보와 경험을 연대하여 심리적 고립감을 해소하고 안정적인 정착을 돕는 통합 플랫폼이 필요하다고 판단해 해당 주제를 선정함.|

## ② 성공 기준 가져오기 / Success criteria from Week 3

| 3주차 성공 기준 원문 Original (Week 3) | 모호한 표현 Vague words |
|---|---|
| *(예시) 학생들이 과제 제출 현황을 쉽게 확인할 수 있다* | *쉽게, 확인할 수 있다* |
| 유학생 개인 조건(국적, 비자, 거주형태 등)에 맞춘 개인화된 준비 타임라인을 생성하고, 학사 공지를 대상, 마감, 행동 중심으로 요약 안내함으로써 유학생에게 필요한 정보를 카테고리화할 때 해당 개인에게 배정되면 성공| 필요한, 잘 배정되면 |
| 내·외국인 학생이 다국어 커뮤니티에서 학교생활과 지역 정보를 자유롭게 질문하고 공유하여, 유학생의 미해결 질문을 낮추고, 타국 생활 적응도를 높임으로써 심리적 고립감을 해소하면 성공| 자유롭게, 낮추고, 높임으로써, 해소하면| 

## ③ Acceptance Criteria

최소 정상 경로 2개 + 실패 경로 1개. **판정 방법** 칸이 비면 아직 명세가 아닙니다.
At least two normal paths + one failure path. If "How to check" is empty, it is not yet a spec.

| # | 경로 Path | EARS 문장 Sentence | 판정 방법 How to check |
|---|---|---|---|
| *예시* | *정상* | *WHEN 학생이 과제 목록을 열면 THE 시스템은 SHALL 과목별 미제출 과제를 마감일 순으로 표시한다* | *미제출 과제 3건을 만든 뒤 목록을 열어 마감일 순으로 나오는지 확인* |
| AC-1 | 정상 Normal | WHEN  THE  SHALL  |  |
| AC-2 | 정상 Normal | WHEN  THE  SHALL  |  |
| AC-3 | 실패 Failure | IF  THEN THE  SHALL  |  |

> 확인할 동작이 더 있으면 AC-4부터 행을 추가해 쓰십시오.
> If there are more behaviors to check, add rows from AC-4.

- [ ] 이번 활동에서 AI를 사용했다면 `PROMPTS.md`에 기록했습니다 / Logged any AI use in `PROMPTS.md`

---

> 수업 종료 시 커밋하세요 / Commit this at the end of class
> `git add docs/week-04.md && git commit -m "docs: 4주차 활동지 작성"`
