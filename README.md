# github-page

### https://\<username\>.github.io 에 리액트 앱 올리기

1. git repository 등록하기

```bash
git remote add origin https://<github repository url>.git
```

2. `gh-pages` 설치

```
npm install --save gh-pages
```

3. `package.json` 에 내용 추가

```json
{
  "homepage": "https://<username>.github.io",  /*upload to user page*/
  "homepage": "https://<username>.github.io/app-name", /*upload to specific app path*/
  "homepage": "https://mywebsite.com", /*or upload to custom domain*/
  
  "scripts": {
    "predeploy": "npm run build",  /*this command will be automatically run before deploy command*/
    "deploy": "gh-pages -d build",
  }
}
```

4. `npm run deploy` 커맨드 실행
5. 등록한 repository 에서 `gh-pages` branch 를 Github Page Source 로 등록

![gh-page-source](https://user-images.githubusercontent.com/20259189/167630137-760afde5-e753-4bf6-afce-0890ed9c9ab5.png)

