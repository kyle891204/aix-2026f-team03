# Week 07 팀 활동지 / Team Activity

| 팀명 / Team | 작성일 / Date | 참여자 / Members |
|---|---|---|
| 팀삼 | 20261014 | 강수연, 김용태, 송선우, 이재림 |

## 1. 아키텍처 다이어그램 / Architecture Diagram

손그림 사진을 올리고 링크하십시오 / Upload a photo and link it.
<img width="2064" height="1300" alt="image" src="https://github.com/user-attachments/assets/6f828140-829c-4fca-a364-23c97551f936" />


| 계층 / Layer | 모듈·파일 / Modules | 의존하지 않는 것 / Does not depend on |
|---|---|---|
| 표현 / Presentation | 현재: ProfilePage.tsx, NoticePage.tsx, CommunityPage.tsx,<br/>공통 API 호출: shared/api/client.ts<br/><br/>공통예정: AppLayout.tsx(공통화면구조), SchoolLifeSwitch.tsx(학교, LIFE전환), ProfilePanel.tsx(개인정보펼침,수정), LanguageSelector.tsx(선호언어설정)<br/><br/><br/>학교예정: SchoolDashboardPage.tsx(학교맞춤공지), PreparationPage.tsx(입국,출국준비), NoticeListPage.tsx, NoticeDetailPage.tsx(전체공지목록,상세), CourseNoticePage.tsx(과목알림), SchedulePage.tsx(학사일정,개인일정관련)<br/><br/>LIFE예정: LifeHomePage.tsx, CommunityListPage.tsx, PostEditorPage.tsx, PostDetailPage.tsx(자유, 장터, 질문 게시판), FacilityPage.tsx(주변편의시설), EmergencyContactPage.tsx(긴급연락처)|DB테이블 SQL, Repository구현, LMS AI 지도 공급자의 연동 방식과 비밀키에 직접 의존하지 않는다.<br/>공지의 사용자 해당 여부, 번역처리, 입출국 준비 항목 생성 같은 업무 판단을 화면에서 직접 처리하지 않는다. 화면은 백엔드api가 제공하는 데이터를 표시하고 사용자의 입력을 전달한다. |
| 로직 / Logic |API 경계 예정: ProfileController, SchoolController, CommunityController, LifeInfoController -> 요청 검증 및 서비스 호출<br/><br/>공통예정: ProfileService(프로필, 선호 언어 검증, 조회, 저장, 수정<br/>AuthService - 로그인과 열람, 수정 권한 확인<br/><br/>학교예정: PreparationService(입국출국예정일과체크리스트정리)<br/>NoticeAnalysisService (공지 대상, 마감, 행동, 서류 추출), MatchingService(프로필과 공지 조건 비교 및 해당 이유 생성), CourseNoticeService(과목별공지, 과제, 학습자료 처리), ScheduleService(공지 학사일정 조회와 개인 일정 저장)<br/> <br/>Life예정: CommunityService(자유, 장터, 질문 게시판과 글 답변 처리), TranslationService(학교 공지와 life 글, 답글 번역, 원문 보존 실패 재시도),<br/>FacilityService(지역별 병원, 마트, 약국 정보처리), EmergencyContactService(현재 국가와 사용자 국적에 맞는 긴급연락처 제공)|React 컴포넌트, css, 화면 배치, 라우팅에 의존하지 않는다.<br/>특정 DB의 SQL이나 LMS, AI, 지도 공급자의 통신 방식에 직접 의존하지 않는다. 저장 조회와 외부 요청은 Repository, Adapter 인터페이스를 통해 처리한다. |
| 데이터 / Data |현재: HanyangLmsClient.java(lms 과목 공지 및 과제 조회)<br/><br/>저장소 예정: ProfileRepository, ReparationRepository, NoticeRepository, ScheduleRepository, PostRepository, CommentRepository, TranslationRepository, FacilityRepository, EmergencyContactRepository<br/><br/>외부 연동 예정: SchoolNoticeAdapter(학교, 국제처, 단과대 공개 공지 수집, LlmAdapter(공지 분석, 요약, 번역 요청과 응답 처리), MapAdapter(시설 위치, 주소 운영시간 조회), OfficialContactAdapter(112, 119와 국적별 대사관, 영사관 정보 조회) |화면 구성, React 상태, 사용자의 클릭 순서에 의존하지 않는다.<br/>공지의 사용자 해당 여부, 일정 저장 여부, 번역 대상 결정 같은 업무 판단을 직접 처리하지 않는다. 저장소와 외부 서비스의 데이터를 조회, 저장하고 외부 응답을 공통 데이터 형식으로 변환하는 역할을 담당한다.<br/|

## 2. 이슈 / Issues

> 이슈 = **앞으로 할 일** / An issue is work to be done.
> 개발할 때 커밋에 이슈 번호를 붙이고(`#3 알레르기 필터 추가`), 완료 조건을 만족하면 이슈를 닫습니다.
> Add the issue number to commits, and close the issue when its criteria are met.

| # | 제목 / Title | 라벨 / Label | 담당 / Assignee | 완료 조건 / Acceptance Criteria |
|---|---|---|---|---|
| **#1** | 학교·LIFE 화면 전환 구현 | frontend | 미정 | 학교/LIFE 선택 시 해당 영역의 홈과 메뉴가 표시되고, 새로고침 후에도 마지막 선택 영역이 유지된다. |
| **#2** | 개인정보·언어 설정 저장 | frontend, backend | 미정 | 학과·학번·국적·현재 비자·학위과정·학년·선호 언어가 저장되어 재접속 후에도 유지되고, 개인정보 영역을 펼치거나 접을 수 있다. 현재 비자는 없음/모름도 선택할 수 있다. |
| **#3** | 맞춤형 학교 대시보드 구현 | frontend, backend | 미정 | 저장된 국적·비자·학위과정·학년 조건과 일치하는 공지가 대시보드에 표시되고, 각 공지에 해당 이유가 함께 표시된다. |
| **#4** | 입출국·비자 맞춤 안내 및 준비 체크리스트 구현 | frontend, backend, data | 미정 | 국적·입국 목적·학위과정·예정 체류기간 등 지원 조건에 따라 검토 대상 비자 유형·해당 이유·준비 서류·절차·공식 출처가 표시된다. 정보 부족·미지원 조건은 확인 필요로 안내한다. 입국/출국 준비를 구분하고 예정일·항목별 완료 상태를 저장·재조회할 수 있다. |
| **#5** | 전체공지 분류·상세 화면 구현 | frontend, backend | 미정 | 학교·국제처·단과대 공지를 구분해 조회할 수 있고, 상세 화면에 대상·마감·해야 할 일·준비 서류·원문이 표시된다. |
| **#6** | 과목알림 조회 기능 구현 | frontend, backend | 미정 | 수강 과목별 공지·과제·학습자료가 구분되고, 과제명과 마감일이 표시된다. |
| **#7** | 학사일정 조회·개인 일정 저장 | frontend, backend | 미정 | 학교 공식 일정과 개인 저장 일정이 구분되어 표시되고, 선택한 공지·과제의 마감일을 저장할 수 있다. 같은 항목을 반복 저장해도 중복 생성되지 않는다. |
| **#8** | LIFE 게시판 분류·목록 구현 | frontend, backend | 미정 | 자유·장터·질문 게시판을 선택하면 해당 게시판의 글만 목록에 표시된다. |
| **#9** | 게시글·답글 작성 및 저장 | frontend, backend | 미정 | 선택한 언어로 글과 답글을 작성하면 작성자·작성 언어·작성 시각과 함께 저장되고, 재접속 후에도 다시 조회할 수 있다. |
| **#10** | 글·답글 자동번역 구현 | AI, backend, frontend | 미정 | 글과 답글이 조회자의 선호 언어로 실제 자동번역되고, 원문과 번역문을 전환할 수 있다. 번역 실패 시 원문과 재시도 버튼이 표시되며 재시도가 동작한다. |
| **#11** | 장터 게시글 거래 정보 구현 | frontend, backend | 미정 | 판매/구매 유형·가격·거래 상태를 입력·저장할 수 있고, 목록과 상세 화면에 해당 정보가 표시된다. |
| **#12** | 주변 편의시설 위치 안내 | frontend, data | 미정 | 지역과 병원·마트·약국 유형을 선택하면 해당 시설 목록이 표시되고, 선택한 시설의 주소·운영시간·연락처를 확인할 수 있다. |
| **#13** | 긴급 연락처 안내 | frontend, data | 미정 | 대한민국 경찰·소방·구급 연락처가 표시되고, 사용자 국적을 선택하면 해당 국가의 공식 대사관·영사관 연락처가 표시된다. |
| **#14** | 실행패키지 생성 | frontend, backend, release | 미정 | 합의한 배포 방식에 따라 프론트·백엔드 실행 산출물과 필요한 구성 파일을 준비하고, 안내된 절차로 서비스가 정상 실행된다. |
| **#15** | 실행·환경설정·운영 문서 작성 | documentation | 미정 | 설치 조건·환경변수 예시·실행 순서·DB 초기화·외부 API 설정을 문서화한다. 비자·시설·연락처 자료의 출처·갱신 방법과 알려진 제한사항을 포함한다. |
| **#16** | 배포 후보 통합 검증 및 오류 수정 | testing, frontend, backend | 미정 | 배포 후보에서 #1~#13의 완료 조건과 외부 조회·번역 실패, 저장 데이터 유지를 재검증한다. 실행·주요 흐름을 막는 오류를 해결하고 결과를 기록한다. |
| **#17** | 최종 배포 및 다른 환경 실행 검증 | release, testing | 미정 | 최종 패키지·버전·다운로드 위치를 공유한다. 다른 팀원이 문서만 보고 별도 환경에서 설치·실행하고 학교·LIFE 주요 기능을 확인한다. |
| **#18** | 기능 범위·API·데이터 구조 확정 | planning, frontend, backend, data | 미정 | #1~#13의 담당자·화면 흐름·API 요청/응답·저장 항목을 합의한다. 비자 안내의 지원 범위·판별 조건·공식 자료와 번역 지원 언어를 문서화한다. |
| **#19** | 학교·LIFE 전체 기능 통합 | frontend, backend, AI, data | 미정 | 통합 환경에서 #1~#13의 화면·API·저장소·외부 연동이 연결되고, 동일한 사용자 프로필과 선호 언어가 학교·LIFE 양쪽에 적용된다. |
| **#20** | MVP 완료 조건 검수 및 오류 수정 | testing, frontend, backend | 미정 | #1~#13의 완료 조건을 검수하고 결과를 기록한다. 재접속 후 데이터 유지, 조건별 공지·비자 안내, 글·답글 번역과 재시도, 일정 중복 방지를 확인하고 주요 흐름을 막는 오류를 해결한다. |

## 3. 마일스톤 / Milestones

| 마일스톤 / Milestone | 마감 / Due | 포함 이슈 / Issues |
|---|---|---|
| **M1. 기능·설계 확정** | **9주차 · 10/27** | **#1~#13 설계 확정** — 기능별 담당자, 화면 흐름, API·데이터 구조 합의. 특히 **#4 비자 안내의 지원 범위·판별 조건·공식 자료**, **#10 번역 지원 언어** 확정 |
| **M2. 공통 기능·게시판 기본 기능 완료** | **10/30** | **#1, #2, #8, #9** — 학교/LIFE 전환·선택 유지, 개인정보·선호 언어 저장, 게시판 분류, 글·답글 작성·저장·재조회 완료 |
| **M3. 학교·LIFE 핵심 기능 연결** | **10주차 · 11/3** | **#3, #5, #6, #10, #11** — 맞춤 대시보드, 전체공지 상세, 과목알림, 글·답글 자동번역, 장터 정보 구현. **#4의 비자 맞춤 안내 부분** 연결 |
| **M4. 전체 기능 구현·통합 완료** | **11/6** | **#4, #7, #12, #13** — 비자 안내와 입출국 체크리스트 통합·저장, 학사일정·개인 일정, 편의시설·긴급 연락처 완료. **#1~#13 전체를 통합 환경에서 실행** |
| **M5. MVP 완료 — 고정 마감** | **11주차 · 11/10** | **#1~#13 완료 조건 검수 통과** — 저장·재조회, 조건별 안내, 실제 번역·원문 전환·재시도, 일정 중복 방지 등을 검증하고 주요 흐름을 막는 오류 해결 |
| **M6. 실행패키지 후보·문서 완성** | **12주차 · 11/17** | **#14, #15 및 #16 1차 검증** — 실행패키지 후보 생성, 설치·설정·운영 문서 작성, 배포 후보에서 전체 기능 재검증 |
| **M7. 내부 배포·다른 환경 실행 검증** | **11/20** | **#16 오류 수정, #17 사전 검증** — 다른 팀원이 문서에 따라 설치·실행하고 학교·LIFE 주요 기능 확인. 발견된 문제 수정 |
| **M8. 실행패키지 배포 완료 — 고정 마감** | **13주차 · 11/24** | **#14~#17 완료** — 최종 패키지 배포, 버전·다운로드 위치 기록, 다른 환경 실행 검증 통과, 제한사항·데이터 갱신 방법 인계 |



> AI를 사용했다면 `PROMPTS.md`에 기록 / Log any AI use in `PROMPTS.md`
