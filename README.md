# org-diagnosis

조직진단 사전 인터뷰 앱의 **진짜 프론트엔드**(완전한 HTML/CSS/JS)가 여기에 있습니다. iframe으로 감싸는 방식이 아니라, 이 페이지가 직접 화면을 그리고 fetch()로 Google Apps Script 백엔드(JSON API)를 호출합니다. 데이터(DB)는 여전히 구글 드라이브의 구글시트에만 있습니다.

- 백엔드: Google Apps Script `doGet`/`doPost`가 `?action=...` 기반 JSON API로 동작(`getInitialData`/`saveTextRecord`/`runFinalAIAnalysis`/`saveAnalysisToSheet` 4개 액션).
- 접속 설정이 `ANYONE_ANONYMOUS`로 변경되어(2026-10-08) 로그인 없이도 CORS(`Access-Control-Allow-Origin: *`)가 정상 동작함 - 기존 `ANYONE`은 구글 로그인을 요구해서 fetch 기반 분리와 맞지 않았음.
- 실제 앱 배포 주소가 바뀌면(새 컨설팅 건) `index.html` 맨 아래 스크립트의 `API_BASE` 상수 한 곳만 새 배포 주소로 바꿔서 다시 커밋하면 됩니다.
- 관리자(최종 분석 탭) 접근: `?admin=1`을 주소 끝에 붙여서 접속(예: `https://jinhyun-jang.github.io/org-diagnosis/?admin=1`).
