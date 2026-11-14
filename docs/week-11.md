# 11주차 활동지 / Week 11 Worksheet

**개발 착수 / Starting development**

- 작성일 / Date: 
- 참여자 / Present: 

---

## ① 착수 점검표 / Start checklist

수업 시작 후 10분 안에 확인합니다. 체크되지 않은 항목이 있으면 그것부터 해결하고 개발을 시작합니다.
*Check within the first 10 minutes. Fix any unchecked item before you start coding.*

- [x] 초기 파일이 저장소에 올라와 있다 / Initial files are in the repository
- [x] 7주차 이슈가 GitHub에 등록되어 있고 담당자가 지정되어 있다 / Week 7 issues are on GitHub with owners
- [x] 팀원 모두 같은 환경에서 실행된다 / Everyone can run it in the same environment
- [x] 브랜치 규칙을 정했다 / Branch rule agreed — 

---

## ② 개발 일정 / Development schedule

- 선행 이슈가 끝나기 전에 뒤 이슈를 넣지 않습니다. / Never schedule an issue before the ones it depends on.
- 한 사람에게 몰리지 않았는지 확인합니다. / Check that no one is overloaded.

| 주차 Week | 수업 일정 Class | 끝낼 이슈 # Issues to close | 담당 Owner |
|---|---|---|---|
| 9주차 | 개발 착수 | #21 기능 범위·API·데이터 구조 확정<br>#27 로그인·#30 회원가입<br>#4 학교·LIFE 전환·#5 프로필 및 언어 설정<br>#11·#12 게시판 구현 착수<br>Gemini·Canvas API 선행 작업 | 김용태: #21·#27·#30·#4·#5·Gemini 설정<br>송선우, 김용태: #11·#12<br>강수연, 이재림: Canvas 설정 |
| 10주차 | 막힘 진단 · 데모 시나리오 초안 | #6 대시보드 1차 구현<br>#7 입출국 준비·#8 전체공지 및 실제 공지 수집<br>#9 과목알림·#10 학사일정 조회·저장<br>#13 번역·#14 장터 거래 정보<br>#15 편의시설 지도·#16 긴급 연락처<br>#37 공통 API 및 인증·CSRF 보완 | 이재림: #6·#9·#10·#37<br>강수연: #7·#8·서버 CSRF<br>김용태: #13·#15·#16<br>송선우, 김용태: #14<br>전원: 통합 점검 |
| 11주차 | **MVP 완료 · 중간 데모** | #45 실제 공지 대시보드 연결<br>#7·#8 공지 AI 분석 보완<br>#15 편의시설 지도·목록 보완<br>학교 화면 다국어 적용<br>#10 공지·과제 마감 저장 연동<br>#23 MVP 검수·오류 수정 | 이재림: #45<br>강수연: 공지 분석·일정 저장 연동<br>김용태: 다국어 UI·수집 오류 보완<br>송선우: 편의시설·번역 재시도 보완<br>전원: #23 검수 |
| 12주차 | 핵심 경로 테스트 | #23 잔여 검수<br>#19 배포 후보 통합 검증·오류 수정<br>#18 실행·환경설정·운영 문서 작성 | 전원: #23·#19<br>이재림: #18 |
| 13주차 | **배포 · 실행 패키지** | #17 최종 실행 패키지 생성<br>#20 최종 배포·다른 환경 실행 검증<br>접속 주소·실행 산출물·문서 공유 | 강수연, 이재림: #17<br>김용태, 강수연: #20 |

> 일정이 맞지 않으면 기능을 줄입니다. 뺀 기능은 5주차 Won't 목록에 옮깁니다.
> *If it doesn't fit, cut scope and move the feature to your Week 5 Won't list.*

---

## ③ 이번 주 목표 이슈 / This week's issues

| # | 제목 Title | 담당 Owner | 완료 Done |
|---|---|---|---|
| #7·#8 | 공지 AI 분석 연결 및 맞춤 안내 최종 검수 | 강수연 | [x] |
| #45 | 맞춤형 대시보드에 실제 학교 공지 연결 | 이재림 | [x] |
| #13 후속 | 다국어 예시 추가 및 번역 재시도 오류 수정 | 송선우 | [x] |
| #15 | 주변 편의시설 지도·목록·전체 보기 보완 | 송선우, 김용태 | [x] |
| 관련 후속 작업 | 학교 공지 수집 시간제한·재시도 보완 | 김용태 | [x] |
| #5 후속 | 학교 화면에 한국어·영어·중국어 UI 적용 | 김용태 | [x] |
| #10 후속 | 공지·과제 마감의 개인 일정 저장 연동 | 강수연 | [x] |
| #23 | MVP 완료 조건 검수 및 오류 수정 | 전원 | [x] |

---

## ④ 오늘 진행한 것 / Progress today
- 배포 환경의 학교 공지 수집 오류를 점검하고 시간제한, 재시도, 진단 로그를 보완함.
- 실제 공지의 대상, 마감, 할일, 준비 서류를 AI로 분석하고 대시보드에 실제 공지를 연결함.
- 비자 정보가 없어 대상 여부를 판단하기 어려운 공지는 '확인 필요'로 안내하기로 함.
- 학교 화면에 한국어, 영어, 중국어 ui를 적용하고 편의시설 지도, 편의시설 목록과 번역 재시도 기능을 보완함.
- 공지, 과제 마감을 개인 일정에 저장하는 기능을 구현함. 호출 한도를 고려하여 과목 공지의 마감은 규칙으로 찾기로 했고, PR리뷰에서 발견된 오류와 충돌은 수정중임.
- 중간 개발 현황 공유 및 PR별 테스트 진행함.
- [ ] 이번 활동에서 AI를 사용했다면 `PROMPTS.md`에 기록했습니다 / Logged any AI use in `PROMPTS.md`

---

> 수업 종료 시 커밋하세요 / Commit this at the end of class
> `git add docs/week-09.md && git commit -m "docs: 11주차 활동지 작성"`
