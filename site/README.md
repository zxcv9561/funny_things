# 만든 것들 모음

직접 만져 보고 재 보는 한 장짜리 판 50개.
물리·수학·생물·소리·구조·양자까지 — 모든 계산은 **브라우저 안에서 그 자리에서** 돌아갑니다.
각 판 끝에는 **검산 과정**과 **만들면서 틀렸던 것**이 함께 적혀 있습니다.

## 구조

```
index.html     목록 · 검색 · 분류 · 안에서 바로 열어 보기
items.json     판 목록 (제목 · 분류 · 설명)
p/<이름>.html   판 하나하나 (각각 외부 연결 없이 혼자 도는 한 장짜리 HTML)
.nojekyll      GitHub Pages 의 Jekyll 처리 끄기
404.html
```

판 하나를 그냥 내려받아 두 번 눌러도 열립니다. 인터넷도 필요 없어요
(「지금 이 순간의 지구」 한 판만 예외로 실시간 자료를 받아 옵니다).

## GitHub Pages 로 올리기

1. GitHub 에서 새 저장소를 만듭니다 (Public).
2. 이 폴더에서:

```bash
git init -b main
git add -A
git commit -m "만든 것들 모음 50개"
git remote add origin https://github.com/<아이디>/<저장소이름>.git
git push -u origin main
```

3. 저장소 → **Settings → Pages** → Source 를 **Deploy from a branch**,
   Branch 를 **main / (root)** 로 두고 저장합니다.
4. 1~2분 뒤 `https://<아이디>.github.io/<저장소이름>/` 에서 열립니다.

저장소 이름을 `<아이디>.github.io` 로 만들면 주소가 `https://<아이디>.github.io/` 가 됩니다.

## 판 하나 주소

목록에서 판을 열면 주소가 `?p=<이름>` 으로 바뀝니다. 그대로 복사해 공유하면 됩니다.
판 자체의 직접 주소는 `p/<이름>.html` 이고요.

## 나중에 판을 더할 때

1. `p/` 에 새 HTML 을 넣고
2. `items.json` 에 `{"k":"파일이름","n":"제목","t":"분류","d":"설명"}` 한 줄을 더한 뒤
3. 다시 push 하면 끝입니다. `index.html` 은 손댈 필요가 없습니다.

> `index.html` 안에도 같은 목록이 한 벌 박혀 있습니다. 웹 주소가 아니라 파일을 직접 두 번 눌러 열었을 때
> 목록이 보이게 하려는 용도예요. 웹에서는 `items.json` 쪽이 우선이라 그대로 두셔도 됩니다.

---

Claude 와 함께 만들었습니다.
