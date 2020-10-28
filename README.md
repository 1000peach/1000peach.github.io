# React App GitHub 호스팅하기

### ✏ React App을 GitHub 호스팅을 이용하여 배포하는 방법

1. GitHub 저장소 생성
2. React App 생성
```
$ create-react-app [React App 이름]
```
3. React App에서 불필요한 내용 제거 후 commit
4. React App과 GitHub 저장소 연결 후 push
```
$ git remote add origin [GitHub 저장소 주소]
$ git push origin master
```
5. React App에 배포를 위한 `gh-pages` 설치
```
$ npm install gh-pages --save-dev
```
6. package.json 파일에 접속할 홈페이지 주소 추가
```
{
    "homepage": "http://[사용자 아이디].github.io/[GitHub 저장소 이름]"
}
```
7. package.json 파일의 script에 predeploy, deploy 추가 후 commit & push
```
{
    "scripts": {
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build"
    }
}
```
8. 배포 명령어 실행
```
$ npm run deploy
```
9. GitHub 저장소의 setting -> GitHub Pages -> sourch에서 branch를 master에서 gh-pages로 변경
10. 몇 분 내로 배포 완료!

### 🔗 참고

* [Velog - GitHub Pages 배포하기](https://velog.io/@byjihye/react-github-pages)