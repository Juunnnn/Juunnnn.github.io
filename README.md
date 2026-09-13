# 이성준 Portfolio

로봇 기구 설계 포트폴리오 웹페이지입니다. 별도의 빌드 과정 없이 정적 파일만으로 동작합니다.

```
.
├── index.html          # 페이지 전체 (HTML + CSS + JS 한 파일)
├── Portfolio_LIG.pdf       # 포트폴리오 PDF
├── Resume_SungjunLee.pdf   # 이력서 PDF
├── img/                # PDF에서 추출한 이미지 20장
└── README.md
```

## GitHub Pages에 올리기

1. GitHub에서 새 저장소를 만듭니다. 이름을 `아이디.github.io`로 하면 주소가 `https://아이디.github.io`가 되고, 다른 이름(예: `portfolio`)으로 하면 `https://아이디.github.io/portfolio`가 됩니다.
2. 이 폴더 안의 파일을 저장소 최상단에 올립니다. 웹에서 올릴 때는 저장소 화면의 **Add file → Upload files**에 폴더째 끌어다 놓으면 됩니다.
3. 터미널을 쓴다면:

   ```bash
   git init
   git add .
   git commit -m "Add portfolio site"
   git branch -M main
   git remote add origin https://github.com/아이디/저장소이름.git
   git push -u origin main
   ```

4. 저장소의 **Settings → Pages**에서 Source를 `Deploy from a branch`, 브랜치를 `main`, 폴더를 `/ (root)`로 지정하고 저장합니다.
5. 1~2분 뒤 주소가 활성화됩니다.

`index.html`이 반드시 저장소 최상단에 있어야 합니다. `site` 같은 폴더 안에 들어가 있으면 페이지가 열리지 않습니다.

## 수정할 때

- 글 내용, 연락처, 링크: `index.html`의 해당 문단을 직접 고치면 됩니다.
- 색상과 여백: `index.html` 위쪽 `:root` 블록의 값(`--navy`, `--blue`, `--mist` 등)만 바꾸면 전체에 반영됩니다.
- 이미지 교체: `img/` 안의 같은 이름으로 덮어쓰면 됩니다.
- 이력서 PDF 교체: 따로 만든 이력서 파일이 있으면 `Resume_SungjunLee.pdf`를 같은 이름으로 덮어쓰면 됩니다. 이름을 바꾸고 싶다면 `index.html`에서 `Resume_SungjunLee.pdf`를 검색해 두 군데(상단 버튼, 마지막 화면 버튼)를 함께 고쳐주세요.
- 프로젝트 추가: `01`, `02`, `03` 섹션 중 하나를 통째로 복사한 뒤 `id`와 상단 네비게이션 링크를 함께 바꿔주세요.

한글 글꼴은 Pretendard를 CDN에서 불러옵니다. 인터넷이 차단된 환경에서 볼 일이 있다면 글꼴 파일을 받아 저장소에 함께 올리고 `<link>` 주소를 바꾸면 됩니다.
