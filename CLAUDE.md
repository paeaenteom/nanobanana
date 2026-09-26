# NanoBanana
> Gemini API(Nano Banana 모델)로 이미지를 생성하는 단일 페이지 웹앱 — Claude의 일: index.html 기능 추가·UI 수정

## 기술 스택
- 순수 HTML/CSS/JS (빌드·프레임워크·패키지 없음)
- Gemini API `generateContent` (브라우저에서 직접 호출)
- 저장: localStorage(API 키 `nb_key`), IndexedDB(생성 이미지)
- 배포: Vercel 정적 호스팅

## 구조
index.html   # 앱 전체: <style> → 마크업 → <script>
vercel.json  # SPA rewrite + 보안 헤더
README.md    # 사용자용 소개

## 명령어
- 로컬: `python3 -m http.server 8000` → http://localhost:8000
- 배포: `vercel --prod`

## 규칙
- JS: ES5 스타일 유지 (`var`, `function`, `.then`), camelCase
- CSS: `:root` 변수(`--bg`, `--yellow` 등) 사용, 한 줄 압축 표기
- UI 문구는 한국어

## 주의
- API 키는 사용자 브라우저에만 저장. 코드나 커밋에 키를 넣지 말 것
- 모델 목록은 `#modelSel`의 `<option>`에서 관리
