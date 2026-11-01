# 🪞 진실의 거울

"거울아 거울아, 세상에서 가장 ○○한 사람은 누구니?"
질문을 고르면 거울이 한참 고민하다가… 마지막에 **전면 카메라로 본인 얼굴**을 비춰주는 장난용 웹앱.

- 질문: 가장 부자 💰 / 가장 예쁜 ✨ / 가장 귀여운 🐣 / 가장 못생긴 👹 + 직접 입력
- 못생긴/바보 같은 질문이면 빨간 화면 + 흔들림 + 💩 비
- 한국어 음성(TTS) + 효과음 (오른쪽 위 🔊로 끄기)
- 📸 결과를 거울 프레임 사진으로 저장/공유
- 카메라 영상은 브라우저 안에서만 쓰이고 어디로도 전송되지 않음

## GitHub Pages로 배포

카메라는 **HTTPS**에서만 켜지는데, GitHub Pages는 기본이 HTTPS라 그대로 동작합니다.

1. GitHub에서 새 저장소 만들기 (예: `mirror`)
2. 이 폴더를 올리기

   ```bash
   git init
   git add .
   git commit -m "진실의 거울"
   git branch -M main
   git remote add origin https://github.com/<아이디>/mirror.git
   git push -u origin main
   ```

3. 저장소 **Settings → Pages → Source: Deploy from a branch → main / (root)** 저장
4. 1~2분 뒤 `https://<아이디>.github.io/mirror/` 접속

## 로컬에서 보기

```bash
python -m http.server 8080
```

`http://localhost:8080` (localhost는 HTTP여도 카메라 허용됨)

## DOPA# 브랜드 프레임

`dopasharp/` 폴더는 모든 DOPASHARP 게임 저장소에 **똑같이** 복사해 쓰는 공통 디자인 시스템(v1.0)입니다. 원본은 `soju-game/dopasharp/`이고, 여기서 고치지 말고 원본을 고친 뒤 모든 저장소에 다시 복사합니다. 게임 화면 색은 각 게임이 유지하고, 시작·결과·공유·다른 게임 이동·하단 브랜드 표시만 통일합니다.

- `tokens.css` — 색상·타이포·여백·모서리·모션 토큰.
- `components.css` — 헤더, 버튼(Primary/Secondary/Tertiary), 게임 카드, 결과 시트, 푸터.
- `dopasharp.js` — 게임 목록(`GAMES`), 결과 시트 `DopaSharp.showResult()`, 다른 게임 시트, 공통 분석 이벤트 `DopaSharp.track()`.

링크 미리보기 이미지는 `og/mirror.html`을 고친 뒤 `og/mirror.png`로 다시 렌더링합니다 (명령은 파일 맨 위 주석 참고).
