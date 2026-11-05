# 검지 베기 (Fruit Slash)

웹캠으로 검지 손가락을 인식해 과일을 자르는 아케이드 웹 게임입니다. 설치 없이 브라우저에서 실행됩니다.

## 플레이 방법

1. 시작 화면에서 모드를 고르고 **카메라 켜고 손 인식 테스트**를 눌러 카메라를 허용합니다.
2. **게임 시작**을 누르고, 카메라 앞에서 검지를 빠르게 움직여 과일을 자릅니다. 💣 폭탄은 피하세요.
3. 에너지가 가득 차면 **양손 검지를 동시에 빠르게** 움직여 특수 공격을 씁니다.
4. 카메라를 켜지 않으면 마우스/터치 드래그로 연습할 수 있습니다.

게임 모드: 타임 어택 · 서바이벌 · 엔드리스 · 하이브리드

## GitHub Pages로 게시하기 (카메라는 https 주소에서만 동작합니다)

1. GitHub에서 **New repository**로 저장소를 만듭니다 (예: `fruit-slash`, Public).
2. **Add file → Upload files**로 이 저장소의 `index.html`과 `README.md`를 올리고 **Commit changes**를 누릅니다.
3. **Settings → Pages**에서 Source를 **Deploy from a branch**, Branch를 `main` / `(root)`로 선택하고 Save를 누릅니다.
4. 1~2분 뒤 `https://<내 GitHub 아이디>.github.io/fruit-slash/` 주소로 접속합니다.

## 알아 둘 점

- 손 인식에는 [MediaPipe Tasks Vision](https://github.com/google-ai-edge/mediapipe) (Apache-2.0)을 jsDelivr CDN에서, 손 모델 파일은 Google의 MediaPipe 공개 저장소에서 불러옵니다. 첫 실행에는 인터넷이 필요합니다.
- 카메라 영상은 사용자 기기 안에서만 처리되며 저장하거나 전송하지 않습니다.
- 과일·폭탄 그림은 직접 그린 SVG이고, 효과음과 배경음은 Web Audio API로 코드에서 만들어 외부 소리 파일이 없습니다.
- 최고 기록과 설정은 브라우저(localStorage)에만 저장됩니다. 온라인 랭킹은 아직 지원하지 않습니다.
- 현재 미구현: 단계별 튜토리얼, 서비스 워커 캐시/설치형 웹앱(PWA).
