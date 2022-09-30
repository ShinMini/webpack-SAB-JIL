# webpack

## webpack 라이브러리 연습 저장용 깃 repo

# 사용 TECH

* "css-loader": "^6.7.1",   -> css file을 webpack configure파일로 관리
* "d3": "^7.6.1",   -> data를 받아와 web에서 graphic 작업을 수행할떄 용의, html canvas와 img 방식으로 원하는 graphe 생성해줌.
* "html-webpack-plugin": "^5.5.0",  -> html에 webpack library를 연결할 때 연결할 links들을 webpack configure에서 관리해줌.
* "json5": "^2.2.1",  -> wwebpack library에서 .json5 data를 handling 하기 편하게 도와줌.
* "papaparse": "^5.3.2",  -> csv file을 object, array 혹은 string등 다양한 형식으로 csv 파일을 받아와 후처리하는데 편했음. 
* "style-loader": "^3.3.1", -> css-loader와 역할 동의
* "toml": "^3.0.0", -> webpack library에서 .toml data를 handling 하기 편하게 도와줌.
* "webpack": "^5.74.0", -> webpack library version
* "webpack-cli": "^4.10.0", -> ''
* "webpack-dev-middleware": "^5.3.3", -> webpack server생성을 node express 모듈이 지원하는 data type으로 configuration을 만들어 return 해줌. (서버관리하는데 유용했음.)
* "webpack-dev-server": "^4.11.1",  -> webpack live server 생성해주는데, 위와 다르게 간단한 서버 생성 및 테스트 하기에 유용했음. 
* "xml-loader": "^1.2.1", -> webpack library에서 .xml data를 handling 하기 편하게 도와줌.
* "yamljs": "^0.3.0"  -> webpack library에서 .yamljs data를 handling 하기 편하게 도와줌.


# 시간 걸렸던 부분

## 1. server-dev-middleware까지 server.js를 node로 실행  
-> 바보같이 spring-react-rest 연습하던 서버 안꺼둬서 충돌생긴줄 모르고 삽질

## 2. express로 실행하되, configure정보는 webpack으로 설정하기 
-> 이건 쉬웠으나, 신선한 충격이였어서 넣어봄

## 3. csv 파일 읽어와 전처리 후 전송하기  
-> 이건 진짜 오래걸림, webpack library를 활용해 가져온 csv 파일 양식이 어떤식으로 생성되는지 직접확인 하기 어려워 console.dir, typeof(), fileattachment()등 다양한 라이브러리를 사용해 원하는 형식으로 csv 파일 정보를 가져워 d3 library를 활용해 원하는 그래프 형식으로 출력하려 햇으나, 생각보다 파일 양식ㅇ정보를 내 마음대로 다루는게 어려웠음, JSON과 다르게 csv는 직접적으로  data를 바로 변환해주는 library가 많지 않았으며, 오히려 csv를 json형식으로 바꿔서 진행하면 편할것같았으나 마음에 안들어서  계속 시도하던 차 papaparse()라이브러리에서 이를 해결해줌.     

* 기타 webpack 관련 여러 library 뜯어보고 저장.
