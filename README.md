# org-diagnosis

조직진단 사전 인터뷰 앱(Google Apps Script)을 iframe으로 감싸서, 브라우저 주소창에는 계속 이 깔끔한 깃허브 주소만 보이도록 하는 페이지.

실제 앱 주소가 바뀌면(새 컨설팅 건으로 배포 ID가 바뀌는 경우) `index.html` 안의 `AKfycb...` 로 시작하는 URL 두 곳(iframe src, fallback 링크)을 새 주소로 바꿔서 다시 커밋하면 됩니다.
