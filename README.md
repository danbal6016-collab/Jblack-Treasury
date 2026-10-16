# JBlack Treasury

럭셔리하고 다크한 감성의 웹사이트와 앱을 AI와 함께 세공하는 디지털 메종, **JBlack Treasury**의 공식 홈페이지입니다.

> Luxurious. Dark. Aesthetic. And yet, real.

## 구성

빌드 과정 없이 `index.html` 한 파일로 동작하는 정적 사이트입니다.

- **Hero**: 골드 필기체 크레스트 로고와 WebGL 실크 배경
- **On Display**: 운영 중인 JBlack Tarot, 다음 공개작 Rate Your Life
- **The Collection**: 18개 작품 카드와 카테고리 필터
- **바로가기 창**: 메뉴의 `바로가기` 버튼이나 `⌘K` / `Ctrl K`로 열고, 이름이나 키워드로 검색
- **The Ledger / The Maison**: 브랜드 철학과 서비스 소개

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
