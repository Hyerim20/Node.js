- npm install figlet -g (-g는 내 컴퓨터 전체에 적용)
- package.json (내용을 대략적으로 확인하기 위함)
- package-lock.json (내용을 상세하게 확인하기 위함)
- require(’figlet’) (figlet 모듈을 요구하다.)
- console.log(data) (data를 출력을 한다)
- express모듈 (웹 프레임워크(프론트엔드에서 백엔드로))
- 로컬호스트(내 컴퓨터 ip 표시 안해도 들어갈 수 있음)
- app.get(’/’,()⇒{})   ‘/’:라우팅
- get : HTTP 메소드
- 요청의 목적, 종류를 알리는 수단
    
    -Get 주소창에서 데이터 넘김
    
    -Post 내부적으로 body에 데이터 넘김
    
- ()⇒{}:콜백함수

setTimeout(()⇒console.log(”hello”), 1000//시간초); //100msec뒤에 콜백함수를 실행해라

```jsx
setTimeout(()=>{console.log("5초 지남")}, 5000)
```

 

```jsx
const express = require('express') //express 요구
const app = express()
const port = 3000

app.get('/', function(req, res){ //requse response => 콜백 함수(끝나고 실행할 함수) 함수(parameter)
    res.send('Hello World')
}) //listen을 하고 난 후 expree app에 라우트(기본 route==들어오는 경로에 따라) 주소로 들어왔을 때 ()=>{} 이 함수를 실행하겠다

app.listen(port,()=>{ 
    console.log('Example app listening on port ${port}')
})  //port:들어올 수 있는 입구
    //port가 listen을 하고 있어야 실행 (port마다 다른 프로그램 실행 가능)
    //port 규모가 정해져있음.
	  //3000번 포트에 대해서 듣는 중입니다.. 그 뒤에 '' 이것을 찍어주겠다

//app.listen(3000)
```

ex) GET /dog ⇒ {’sound’ : ‘멍멍’} 

html파일 get으로 보내기 ‘<h1>강아지</h1>’
