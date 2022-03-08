## Type Checking
* 자바스크립트는 타입 체크를 하지 않기 때문에 타입 오류가 발생함
* 이에 타입을 체킹하는 것이 중요하고 도구가 필요함
* 가장 인기가 있는 타입스크립트는 자바스크립트에 타입 정의만 얹어놓은 느낌


```
const someString = 'Hello'
const result = Math.log(someString)
```

위와 같은 경우에 타입에러가 발생함.

### 타입스크립트 사용
* 타입스크립트, eslint 를 설치 후
* 상단에 @ts-check 를 추가하면 타입 체크가 가능

### node에서 타임스크립트 도움받기
* npm install --save-dev @types/node
* vscode가 타입스크립트 바이너리를 이용하여 타입체킹을 도와줌

```
const http = require('http)
const server = http.createServer((req, res)=> {
    res.statusCode = 200
    res.end('Hello!)
})

const PORT = 3000
server.listen(PORT, ()=> {
    console.log(`The Server is listening at port${PORT}`)
})
```

예를 들면 상기의 코드에서 `statusCode`를 문자로 넣거나 오타를 내는 경우 타입체킹으로 오류를 방지할 수 있음