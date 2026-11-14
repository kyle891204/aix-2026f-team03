# 10주차 활동지 / Week 10 Worksheet

**개발 착수 / Starting development**

- 작성일 / Date: 2026.11.10.
- 참여자 / Present: 강수연, 김용태, 송선우, 이재림

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

- 선행 이슈가 끝나기 전에 뒤 이슈를 넣지 않습니다. / Never schedule an issue before the ones it depends on.
- 한 사람에게 몰리지 않았는지 확인합니다. / Check that no one is overloaded.

| 주차 Week | 수업 일정 Class | 끝낼 이슈 # Issues to close | 담당 Owner |
|---|---|---|---|
| 9주차 | 개발 착수 | #21 기능 범위·API·데이터 구조 확정<br>#27 로그인·#30 회원가입<br>#4 학교·LIFE 전환·#5 프로필 및 언어 설정<br>#11·#12 게시판 구현 착수<br>Gemini·Canvas API 선행 작업 | 김용태: #21·#27·#30·#4·#5·Gemini 설정<br>송선우, 김용태: #11·#12<br>강수연, 이재림: Canvas 설정 |
| 10주차 | 막힘 진단 · 데모 시나리오 초안 | #6 맞춤 대시보드 1차 구현<br>#7 입출국 준비·#8 전체공지 및 실제 공지 수집<br>#9 과목알림·#10 학사일정 조회 및 개인 일정 저장<br>#13 커뮤니티 번역·#14 장터 거래 정보<br>#15 편의시설 지도 1차 보완·#16 긴급 연락처<br>#37 공통 API 및 인증·CSRF 보완 | 이재림: #6·#9·#10·#37<br>강수연: #7·#8·서버 CSRF<br>김용태: #13·#15·#16<br>송선우, 김용태: #14<br>전원: 공통 작업 및 통합 점검 |
| 11주차 | **MVP 완료 · 중간 데모** | #22 학교·LIFE 전체 기능 통합<br>실제 공지 AI 분석 및 대시보드 연결<br>학교 화면 다국어 적용<br>공지·과제 마감 저장 연동<br>#23 MVP 완료 조건 검수·오류 수정 | 강수연: 공지 분석·일정 저장 연동<br>이재림: 실제 공지 대시보드 연결<br>김용태: 다국어 UI·배포 환경 점검<br>송선우: 편의시설·번역 후속 보완<br>전원: #22·#23 검수 |
| 12주차 | 핵심 경로 테스트 | #19 배포 후보 통합 검증·오류 수정<br>#18 실행·환경설정·운영 문서 작성<br>학교·LIFE 주요 흐름과 외부 조회·번역 실패 상황 재검증 | 전원: #19<br>이재림: #18 |
| 13주차 | **배포 · 실행 패키지** | #17 최종 실행 패키지 생성<br>#20 최종 배포·다른 환경 실행 검증<br>접속 주소·실행 산출물·환경설정 문서 공유 | 강수연, 이재림: #17<br>김용태, 강수연: #20 |

> 일정이 맞지 않으면 기능을 줄입니다. 뺀 기능은 5주차 Won't 목록에 옮깁니다.
> *If it doesn't fit, cut scope and move the feature to your Week 5 Won't list.*

---

## ③ 이번 주 목표 이슈 / This week's issues

| # | 제목 Title | 담당 Owner | 완료 Done |
|---|---|---|---|
| #11·#12·#14 | LIFE 게시판 목록·게시글·답글·거래 정보 구현 및 통합 점검 | 송선우, 김용태 | [x] |
| #37 | 프런트 공통 API 호출 구조 적용 | 이재림 | [x] |
| 관련 공통 작업 | 서버 공통 CSRF 검사 및 인증·사용자별 데이터 분리 점검 | 강수연, 송선우, 김용태, 이재림 | [x] |
| #6 | 맞춤형 학교 대시보드 1차 구현 — 실제 공지 연결은 후속 작업 | 이재림 | [x] |
| #7 | 입출국 준비 안내·체크리스트 구현 및 맞춤 안내 검수 | 강수연 | [ ] |
| #8 | 전체공지 화면·실제 공지 수집 구현 및 AI 분석 연결 | 강수연 | [ ] |
| #9 | 과목알림 조회 기능 구현 | 이재림 | [x] |
| #10 | 학사일정 조회·개인 일정 저장 구현 — 공지·과제 저장은 후속 작업 | 이재림 | [x] |
| #13 | 게시글·답글 자동번역 및 실패 재시도 구현 | 김용태, 송선우 | [x] |
| #15 | 주변 편의시설 지도 1차 보완 및 목록 연결 | 김용태 | [ ] |
| #16 | 긴급 연락처 조회 기능 구현 | 김용태 | [x] |
| #22 | 학교·LIFE 전체 기능 통합 및 주요 흐름 확인 | 전원 | [ ] |

---

## ④ 오늘 진행한 것 / Progress today
- 공통 API 호출 경로와 인증/CSRF 처리를 보완하고 사용자별 데이터 분리와 수정 권한을 점검함
- 게시판, 과목알림, 입출국 준비, 전체공지, 긴급 연락처 기능을 구현하고, 대시보드를 1차적으로 연결함.
- 실제 학교 공지 수집, 학사일정 조회 및 개인 일정 저장 기능을 구현함.
- 커뮤니티 자동번역, 로그인, 회원가입, LIFE 화면의 다국어 ui를 적용하고 편의시설 지도를 보완함.
- 통합 테스트로 주요 기능을 점검하고 실제 공지 AI 분석과 대시보드 연결은 11주차에 진행하기로 함.


- [ ] 이번 활동에서 AI를 사용했다면 `PROMPTS.md`에 기록했습니다 / Logged any AI use in `PROMPTS.md`

---

> 수업 종료 시 커밋하세요 / Commit this at the end of class
> `git add docs/week-09.md && git commit -m "docs: 10주차 활동지 작성"`
