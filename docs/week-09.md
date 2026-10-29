# 9주차 활동지 / Week 9 Worksheet

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

5주차 **작업 순서**와 7주차 **이슈·마일스톤**을 바탕으로 이슈를 주차별로 배치합니다.
*Place your issues week by week, based on the Week 5 work order and Week 7 issues and milestones.*

- 11주차에 MVP가 동작해야 합니다. / Fill backwards from the deadlines.
- 선행 이슈가 끝나기 전에 뒤 이슈를 넣지 않습니다. / Never schedule an issue before the ones it depends on.
- 한 사람에게 몰리지 않았는지 확인합니다. / Check that no one is overloaded.

| 주차 Week | 수업 일정 Class | 끝낼 이슈 # Issues to close | 담당 Owner |
|---|---|---|---|
| 9주차 | 개발 착수 | #21 기능 범위·API·데이터 구조 확정<br>#4 학교·LIFE 페이지 전환<br>#5 개인정보·선호 언어 저장<br>#11 게시판 분류·목록<br>#12 글·답글 작성·저장 및 질문 해결 상태<br>Gemini·Canvas API 설정 및 호출 검증 — #13·#9의 선행 작업 | 김용태: #21·#4·#5·Gemini 설정<br>송선우, 김용태: #11·#12<br>강수연, 이재림: Canvas 설정 |
| 10주차 | 막힘 진단 · 데모 시나리오 초안 | #8 전체공지 분류·상세·번역<br>#6 맞춤 대시보드<br>#7 입출국·비자 안내·체크리스트<br>#9 과목알림<br>#10 학사일정·개인 일정 저장<br>#13 글·답글 자동번역 및 실패 후 재시도<br>#14 장터 거래 정보·판매중/판매완료 상태<br>#15 편의시설 위치 안내 — 목업 데이터<br>#16 긴급 연락처 안내<br>#22 학교·LIFE 전체 기능 통합 — 개별 기능 완료 후 11/6 목표 | 강수연, 이재림: #8·#6·#9·#10<br>강수연: #7<br>김용태: #13·#15·#16<br>송선우, 김용태: #14<br>이재림: #22 |
| 11주차 | **MVP 완료 · 중간 데모** | #23 MVP 완료 조건 검수·오류 수정<br>로그인·회원가입·동의 저장, 학교·LIFE 주요 흐름, 데이터 유지, 맞춤 안내, 실제 번역·재시도, 일정 중복 방지 확인<br>**11/10까지 MVP 동작 완료** | 강수연, 이재림: #23 |
| 12주차 | 핵심 경로 테스트 | #18 실행·환경설정·운영 문서 작성<br>#19 배포 후보 통합 검증·오류 수정<br>배포 환경에서 학교·LIFE 주요 흐름과 외부 조회·번역 실패 상황 재검증<br>11/17 1차 QA, 11/20 수정·재확인 목표 | 이재림: #18<br>송선우, 김용태, 강수연, 이재림: #19 |
| 13주차 | **배포 · 실행 패키지** | #17 최종 실행 패키지 생성<br>#20 최종 배포·다른 환경 실행 검증<br>Vercel 접속 주소, 프런트·백엔드 실행 산출물, 환경설정·실행 문서 공유<br>다른 팀원이 문서만으로 실행하는 것을 확인하고 **11/24까지 배포 완료** | 강수연, 이재림: #17<br>김용태, 강수연: #20 |

> 일정이 맞지 않으면 기능을 줄입니다. 뺀 기능은 5주차 Won't 목록에 옮깁니다.
> *If it doesn't fit, cut scope and move the feature to your Week 5 Won't list.*

---

## ③ 이번 주 목표 이슈 / This week's issues

| # | 제목 Title | 담당 Owner | 완료 Done |
|---|---|---|---|
| #21 | 기능 범위·API·데이터 구조 확정 | 김용태 | [x] |
| #27 | Google 로그인 기능 구현 | 김용태 | [x] |
| #30 | 회원가입 로직 구현 | 김용태 | [x] |
| #4 | 학교·LIFE 페이지 전환 및 마지막 선택 영역 복원 | 김용태 | [x] |
| #5 | 개인정보·선호 언어 저장 및 재조회 | 김용태 | [x] |
| #11 | 자유·장터·질문 게시판 분류·목록 구현 | 송선우, 김용태 | [ ] |
| #12 | 글·답글 작성·저장 및 질문 해결 상태 저장 | 송선우, 김용태 | [ ] |
| #13의 선행 작업 | Gemini API 설정 및 백엔드 번역 호출 검증 | 김용태 | [ ] |
| #9의 선행 작업 | Canvas API 연동 설정·호출 검증 확인 | 강수연, 이재림 | [ ] |

---

## ④ 오늘 진행한 것 / Progress today

- [ ] 이번 활동에서 AI를 사용했다면 `PROMPTS.md`에 기록했습니다 / Logged any AI use in `PROMPTS.md`
(미사용)

---

> 수업 종료 시 커밋하세요 / Commit this at the end of class
> `git add docs/week-09.md && git commit -m "docs: 9주차 활동지 작성"`
