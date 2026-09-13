# effortball-cloud.github.io

루키(ROOKIE) 안드로이드 앱의 도메인 인증 파일을 두는 자리입니다.

- `/.well-known/assetlinks.json` — 안드로이드 앱(TWA)과 이 도메인을 묶는 파일.
  구글플레이 콘솔의 **앱 서명 키 SHA-256 지문**이 들어가야 합니다. (업로드 키가 아니라 Play가 관리하는 서명 키)
- 앱 본체는 [`/rookie-baseball/`](https://effortball-cloud.github.io/rookie-baseball/) 에 있습니다.

지문이 틀리면 앱 위에 주소창이 뜹니다. 그게 "assetlinks 가 안 맞는다"는 신호입니다.
