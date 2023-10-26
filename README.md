# React 사이트 만들기

## 바로 가기

### 유튜브 강의 바로가기
[유튜브 강의 바로가기](https://www.youtube.com/watch?v=Yoqm5ah7qw4&list=PL4UVBBIc6giLDflw5zDXA-FpYZLwGaY0a&index=1)

### 소스 코드 바로가기
[소스 코드 바로가기](https://webstoryboy.co.kr/1964)

## 시작하기
1. 바탕화면에 `webs-youtube` 폴더 생성하기
2.  터미널에 `npx create-react-app .` 입력 (여기서 .은 폴더명을 뜻함)
3. 설치가 완료되면 `npx start` 입력
4. 리액트 기본 화면이 출력되면 기본세팅은 완료!

## 라이브러리 설치하기
1. `public` 폴더 내 해당 파일 삭제하기

    ![a01](https://prod-files-secure.s3.us-west-2.amazonaws.com/8f612a5f-a317-4a35-b0b5-d8d1627ca205/0bc79e27-1f7e-40ec-b338-35ffa1664429/Untitled.png)
    
2.  `public`에 `favicon.svg` 파일 생성후 아래 코드 넣기
    
    ```html
    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
    	<path fill-rule="evenodd" clip-rule="evenodd" d="M14.2929 5.29289C14.6834 4.90237 15.3166 4.90237 15.7071 5.29289L21.7071 11.2929C22.0976 11.6834 22.0976 12.3166 21.7071 12.7071L15.7071 18.7071C15.3166 19.0976 14.6834 19.0976 14.2929 18.7071C13.9024 18.3166 13.9024 17.6834 14.2929 17.2929L18.5858 13H3C2.44772 13 2 12.5523 2 12C2 11.4477 2.44772 11 3 11H18.5858L14.2929 6.70711C13.9024 6.31658 13.9024 5.68342 14.2929 5.29289Z" fill="black"/>
    </svg>
    ```
    
3. 기존 `spaces` 를 `2` 에서 `4` 로 수정하기
    
    ![a02](https://prod-files-secure.s3.us-west-2.amazonaws.com/8f612a5f-a317-4a35-b0b5-d8d1627ca205/5df74cc1-2ca9-4ff4-b4a8-e8572675e097/Untitled.png)
    
4. `public` 에`index.html` 기본 세팅 
    
    ```html
    <!DOCTYPE html>
    <html lang="ko">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="description" content="유튜브 API를 이용하여 나만의 사이트를 만드는 튜토리얼입니다."/>
        <meta name="keyword" content="포트폴리오, 리액트, react, react.js, 코딩 사이트, 사이트 만들기, 리덕스" />
        <link rel="icon" type="image/svg+xml" href="favicon.svg" />
        <title>나만의 유튜브 코딩 사이트 만들기 🧐</title>
    </head>
    <body>
        <div id="root"></div>
    </body>
    </html>
    ```
    
5. `src` 폴더 내 해당 파일 삭제하기
    
    ![a03](https://prod-files-secure.s3.us-west-2.amazonaws.com/8f612a5f-a317-4a35-b0b5-d8d1627ca205/a538a009-4cfc-4281-9176-3729d0983e68/Untitled.png)
    
6. `src` 에 `App.js`에서 모든 내용 삭제 후 `rafce` 입력
    1. 만약 `rafce` 입력이 안된다면 `es7+ react snippets` 설치
    2. 아이콘 테마는 `material icon Theme` 설치
    
    ```jsx
    import React from 'react'
    
    const App = () => {
      return (
        <div>App</div>
      )
    }
    
    export default App
    ```
    
7. `src` 에 `index.js` 수정하기
    
    ```jsx
    import React from 'react';
    import ReactDOM from 'react-dom/client';
    import App from './App';
    
    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(
        <React.StrictMode>
            <App />
        </React.StrictMode>
    );
    ```
    
8. 설치하기
    
    ```bash
    # react-router-dom을 설치합니다.
    # react는 SPA 이기 때문에 여러가지 페이지를 만들기 위해서 설치해야함
    npm install react-router-dom
    
    # axios를 설치합니다.
    # Axios는 간단하고 강력한 API를 제공하여 HTTP 요청 및 응답을 처리할 수 있도록 도와줍니다
    npm install axios
    
    # react-icons을 설치합니다.
    # FontAwesome, Material Icons, Ionicons 등과 같은 아이콘 라이브러리를 React 애플리케이션에서 사용할 수 있습니다.
    npm install react-icons
    
    # react-player를 설치합니다.
    # YouTube, Vimeo, SoundCloud, Facebook 등과 같은 플랫폼에서 호스팅되는 미디어를 간단하게 재생하고 컨트롤할 수 있습니다.
    npm install react-player
    
    # sass를 설치합니다.
    npm install sass
    
    # react-helmet-async를 설치합니다.
    # 웹 페이지의 제목, 메타 태그, 스타일, 스크립트 등을 동적으로 설정하고 업데이트할 수 있습니다.
    # 검색엔진 최적화에 사용합니다.
    npm install react-helmet-async
    
    # npm install swiper
    # 웹 페이지 또는 모바일 앱에서 이미지 슬라이더, 광고 배너, 컨텐츠 갤러리 등을 만들 수 있습니다.
    npm install swiper
    
    # 한번에 설치하기
    npm install react-router-dom axios react-icons react-player sass react-helmet-async swiper
    ```
    
9. `src` 에 `package.json` 버전 맞추기 (버전 수정 후 반드시 `npm i` 실행)
    
    ```json
    {
      "name": "webs-youtube",
      "version": "0.1.0",
      "private": true,
      "dependencies": {
          "@testing-library/jest-dom": "^5.17.0",
          "@testing-library/react": "^13.4.0",
          "@testing-library/user-event": "^13.5.0",
          "axios": "^1.5.1",
          "react": "^18.2.0",
          "react-dom": "^18.2.0",
          "react-helmet-async": "^1.3.0",
          "react-icons": "^4.11.0",
          "react-player": "^2.13.0",
          "react-router-dom": "^6.16.0",
          "react-scripts": "5.0.1",
          "sass": "^1.69.2",
          "swiper": "^10.3.1",
          "web-vitals": "^2.1.4"
      },
      "scripts": {
          "start": "react-scripts start",
          "build": "react-scripts build",
          "test": "react-scripts test",
          "eject": "react-scripts eject"
      },
      "eslintConfig": {
          "extends": [
          "react-app",
          "react-app/jest"
          ]
      },
      "browserslist": {
          "production": [
          ">0.2%",
          "not dead",
          "not op_mini all"
          ],
          "development": [
          "last 1 chrome version",
          "last 1 firefox version",
          "last 1 safari version"
          ]
      }
    }
    ```







# 나만의 유튜브 사이트 만들기

이 강의는 React 프레임워크와 YouTube API를 이용하여 자신만의 간단한 영상 사이트를 만듭니다. React의 기본 개념을 이해하고, 컴포넌트를 구조화하고 상태를 관리하는 방법을 학습하며, 
YouTube Data API를 활용하여 외부 데이터를 가져오는 방법을 익히고, API 응답을 처리하여 사용자에게 의미 있는 정보를 제공하는 방법을 이해합니다.

## 완성작 보기
미리보기 : 

## 사용스택
- node.js를 설치하고 사용합니다. 
- react를 사용하여 사이트를 완성합니다. 
- youTube Api를 이용하여 데이터를 가져옵니다.
- rapidapi를 이용하여 데이터를 가져옵니다.
- netlify를 통해 사이트를 배포합니다.
- firebase를 통해 사이트를 배포합니다.
- vercel를 통해 사이트를 배포합니다.
- git을 사용하여 파일을 관리합니다.

## 프로젝트 실행
- react를 설치합니다. `npx create-react-app 타이틀`
- react-router-dom을 설치합니다. `npm install react-router-dom`
- axios를 설치합니다. `npm install axios`
- react-icons을 설치합니다. `npm install react-icons`
- react-player를 설치합니다. `npm install react-player`
- sass를 설치합니다. `npm install sass`
- react-helmet-async를 설치합니다. `npm install react-helmet-async`
- swiper를 설치합니다. `npm install swiper`