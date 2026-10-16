# JBlack Treasury

럭셔리하고 다크한 감성의 웹사이트와 앱을 AI와 함께 세공하는 디지털 메종, **JBlack Treasury**의 공식 홈페이지입니다.

> Luxurious. Dark. Aesthetic. And yet, real.

## 구성

빌드 과정 없이 `index.html` 한 파일로 동작하는 정적 사이트입니다.

- **Loader**: 금고 문이 열리듯 카운트업 후 걷히는 인트로
- **Hero**: 서명처럼 써지는 골드 필기체 크레스트 로고와 WebGL 실크 배경
- **Manifesto**: 스크롤에 따라 단어가 하나씩 켜지는 원칙 문장
- **On Display**: 운영 중인 JBlack Tarot, 다음 공개작 Rate Your Life
- **The Collection**: 18개 작품을 가로로 넘겨 보는 고정 갤러리(데스크톱)와 카테고리 필터
- **바로가기 창**: 메뉴의 `바로가기` 버튼이나 `⌘K` / `Ctrl K`로 열고, 이름이나 키워드로 검색
- **The Ledger / The Maison**: 브랜드 철학과 서비스 소개

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
