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
