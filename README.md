# effortball-cloud.github.io

ROOKIE B(루키 비) 안드로이드 앱의 도메인 인증 파일을 두는 자리입니다.

- `/.well-known/assetlinks.json` — 안드로이드 앱(TWA)과 이 도메인을 묶는 파일.
  구글플레이 콘솔의 **앱 서명 키 SHA-256 지문**이 들어가야 합니다. (업로드 키가 아니라 Play가 관리하는 서명 키)
- 앱 본체는 **https://rookieb.com/** 에 있습니다 (2026-10-11 자기 도메인으로 이전, Cloudflare Pages).
  - `404.html` — `/rookieb/…`·`/rookie-baseball/…` 로 들어오면 그 기기의 기록(rookie.* — 로그인 토큰 제외)을 `#rbmig=` 에 담아 rookieb.com 으로 보냅니다. `rookieb` 저장소를 비공개로 돌리면 `/rookieb/` 주소는 이 404 가 받습니다.
  - 안드로이드 앱의 도메인 인증 파일은 이제 `rookieb.com/.well-known/assetlinks.json`(원본 `배포/.well-known/`)이 기준입니다. 이 저장소의 같은 파일은 예전 테스트 APK 용으로 남겨 둡니다.
- 패키지: `io.github.effortball_cloud.rookieb` (2026-10-07부터). 예전 테스트 APK 용 `…rookie` 항목도 당분간 함께 둡니다.

지문이 틀리면 앱 위에 주소창이 뜹니다. 그게 "assetlinks 가 안 맞는다"는 신호입니다.

## 지문 목록

| 지문 | 무엇 | 상태 |
|---|---|---|
| `3B:DA:B6:C5:…:86:1E` | 업로드 키 (친구 테스트용 APK 서명) | ✅ 등록 |
| (미정) | **Play 앱 서명 키** — 콘솔 → 앱 무결성 → 앱 서명 키 인증서 SHA-256 | ⏳ 첫 AAB 업로드 후 추가 |

Play 지문을 안 넣으면 **스토어에서 받은 앱**에 주소창이 뜹니다. 잘못된 형식의 지문을 넣으면 목록 전체가 무효가 될 수 있으니 자리표시자는 넣지 않습니다.
