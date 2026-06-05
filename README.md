인천하늘고 Copilot Studio 챗봇
Copilot Studio 기반 챗봇을 웹에서 사용하기 위한 단일 HTML 클라이언트입니다.  
Microsoft Bot Framework WebChat을 사용하여 Direct Line 방식으로 연결됩니다.
---
프로젝트 구조
```
chatbot (4).html
README.md
```
---
동작 구조
```
Browser
  ↓
WebChat (Bot Framework)
  ↓
Direct Line API
  ↓
Copilot Studio Bot
```
---
실행 방법
로컬 실행
HTML 파일 더블클릭
또는 Live Server 사용
배포
GitHub Pages
Azure Static Web Apps
Vercel
---
설정
HTML 내부에서 TOKEN_ENDPOINT 수정 필요
```js
const TOKEN_ENDPOINT =
  'https://.../directline/token?...';
```
Copilot Studio에서 발급한 Direct Line Token Endpoint로 교체해야 정상 동작함.
---
주요 기능
Copilot Studio 챗봇 연결
실시간 채팅
로딩 화면 표시
새로고침 및 세션 초기화
도움말 메시지 자동 전송
---
UI 구성
헤더
챗봇 이름
상태 표시
새로고침 버튼
채팅 영역
WebChat 렌더링
푸터
도움말 버튼
새 대화 버튼
---
스타일 커스터마이징
색상 변경
```css
:root {
  --pink: #DE8DE2;
  --green: #5A6C3D;
}
```
메시지 스타일 변경
```js
const styleOptions = {
  bubbleBackground: '#faf1fb',
  bubbleFromUserBackground: '#eef2e6'
};
```
---
주의사항
Direct Line Token은 일정 시간 후 만료됨
TOKEN_ENDPOINT 외부 노출 시 보안 위험 존재
HTTPS 환경 권장
CORS 설정 필요할 수 있음
---
확장 가능 기능
급식 알림 (NEIS API)
Adaptive Card 입력 UI
Power Automate 연동
사용자 상태 저장
---
기술 스택
HTML
CSS
JavaScript
Microsoft Bot Framework WebChat
Copilot Studio
Direct Line API
---
요약
이 프로젝트는 백엔드 없이 HTML 하나로 Copilot Studio 챗봇을 웹에 연결하는 최소 구현이다.
```
HTML 1개 = 챗봇 웹앱
```
