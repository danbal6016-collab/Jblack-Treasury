# JBlack Treasury

보석처럼 세공한 웹사이트와 앱을 소장한 디지털 메종, **JBlack Treasury**의 공식 홈페이지입니다.

> Only truth and real.

## 구성

빌드 과정 없이 `index.html` 한 파일로 동작하는 정적 사이트입니다.

- **Intro**: 깊은 보석빛 물감이 수채화처럼 하나씩 번지고 빛이 한 번 쓸고 지나가는 약 5초 인트로. 금박 질감의 "The truth is coming to you..." 문구와 하단 000→100 카운트
- **Hero**: 불 꺼진 대전시실(열주, 아치형 천장, 대리석 바닥, 빛나는 금고 문). 커서가 괴도의 손전등이 되어 전시실과 금빛 로고를 비춤
- **Crystals**: 모든 보석을 WebGL로 실시간 렌더링. 브릴리언트 컷 안에서 빛이 전반사·분산되는 과정을 계산해 진짜 크리스털처럼 반짝임
- **Logo**: 브러시드 골드 질감과 입체 두께가 들어간 JBlack 필기체 로고
- **On Display**: 운영 중인 JBlack Tarot, 다음 공개작 Rate Your Life
- **The Collection**: 18개 작품을 가로로 넘겨 보는 고정 갤러리(데스크톱)와 카테고리 필터
- **The Ledger**: 사람들이 지친 것과 트레저리의 기준
- **Contact**: 누르면 이메일 주소(n6248129@gmail.com)가 복사됨
- **바로가기 창**: 메뉴의 `바로가기` 버튼이나 `⌘K` / `Ctrl K`로 열고, 이름이나 키워드로 검색

## 사용한 라이브러리

CDN에서 불러옵니다: GSAP 3.12.5 + ScrollTrigger(스크롤 연출), Lenis 1.1.13(부드러운 스크롤). 동작 줄이기 설정을 켠 사용자에게는 애니메이션 없이 정적인 화면이 보입니다.

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
