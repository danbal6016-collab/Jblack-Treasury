# JBlack Treasury

보석처럼 세공한 웹사이트와 앱을 소장한 디지털 메종, **JBlack Treasury**의 공식 홈페이지입니다.

> Only truth and real.

## 구성

빌드 과정 없이 `index.html` 한 파일로 동작하는 정적 사이트입니다.

- **Intro**: 보랏빛 금고 문을 향해 어두운 열주 복도를 당당하게 걸어 들어가는 약 5초 인트로. 걸음마다 시점이 흔들리고 문빛이 맥박처럼 뛰며, 깊은 보석빛 물감이 수채화처럼 번지고 빛이 한 번 쓸고 지나감. 금박 질감의 "The truth is coming to you..." 문구와 하단 000→100 카운트
- **Hero**: 불 꺼진 대전시실(열주, 아치형 천장, 대리석 바닥, 빛나는 금고 문). 커서가 괴도의 손전등이 되어 전시실과 금빛 로고를 비춤
- **Crystals**: 모든 보석을 WebGL로 실시간 렌더링. 브릴리언트 컷 안에서 빛이 전반사·분산되는 과정을 계산해 진짜 크리스털처럼 반짝임
- **Logo**: 브러시드 골드 질감과 입체 두께가 들어간 JBlack 필기체 로고
- **Music**: 로고가 나타나는 순간 은은하고 몽환적인 클래식 선율(직접 작곡한 D단조 왈츠, Web Audio로 실시간 연주)이 깔림. 브라우저가 자동 재생을 막으면 화면을 처음 누르는 순간 시작되고, 왼쪽 아래 `Music` 버튼으로 끄고 켤 수 있음
- **Members**: 회원가입 / 로그인과 Treasure Passport(18개 사이트 중 가입한 곳을 보석으로 표시)
- **Notice**: 같은 계정·이메일로 18개 사이트에 모두 가입하면 보물을 모두 모은 것으로 인정되어 각 사이트에서 블랙코인 500개를 준다는 공지
- **On Display**: 운영 중인 JBlack Tarot, 다음 공개작 Rate Your Life(공개 전이라 문구 한 줄만 남기고 모자이크 처리)
- **The Collection**: 18개 작품을 가로로 넘겨 보는 고정 갤러리(데스크톱)와 카테고리 필터
- **The Ledger**: 사람들이 지친 것과 트레저리의 기준
- **Contact**: 누르면 이메일 주소(n6248129@gmail.com)가 복사됨
- **바로가기 창**: 메뉴의 `바로가기` 버튼이나 `⌘K` / `Ctrl K`로 열고, 이름이나 키워드로 검색

## 사용한 라이브러리

CDN에서 불러옵니다: GSAP 3.12.5 + ScrollTrigger(스크롤 연출), Lenis 1.1.13(부드러운 스크롤). 동작 줄이기 설정을 켠 사용자에게는 애니메이션 없이 정적인 화면이 보입니다.

## 회원 시스템 연결하기

지금은 **데모 모드**라서 계정이 방문자 브라우저에만 저장됩니다. 실제로 18개 사이트가 하나의 계정을 쓰려면 [Supabase](https://supabase.com) 프로젝트를 하나 만들고 `index.html`의 `AUTH_CONFIG`에 URL과 anon(공개) 키를 넣으세요.

```js
const AUTH_CONFIG = { supabaseUrl: 'https://xxxx.supabase.co', supabaseAnonKey: 'eyJ...' };
```

18개 사이트가 모두 같은 Supabase 프로젝트로 로그인하고, 가입한 사이트의 lot 번호를 `user_metadata.treasures` 배열에 쌓으면 Treasure Passport에 자동으로 반영됩니다. 18개가 모두 모이면 각 사이트에서 블랙코인 500개를 지급하면 됩니다.

## 새 작품 공개하기

`index.html` 안의 `LOTS` 목록에서 해당 작품의 `status`를 `'open'`으로 바꾸고 `url`에 주소를 넣으면, 카드와 바로가기 창, 개수 표시가 함께 바뀝니다.

```js
{ lot: '02', name: 'Rate Your Life', ..., status: 'open', url: 'https://example.com/' }
```

## 배포

- **Vercel**: 이 저장소를 Import하고 Framework Preset을 `Other`로 두면 그대로 배포됩니다.
- **GitHub Pages**: Settings → Pages에서 `main` 브랜치의 `/ (root)`를 선택합니다.

## 운영 중인 사이트

- JBlack Tarot · https://www.jblacktarot.com/
