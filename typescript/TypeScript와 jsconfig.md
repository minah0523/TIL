### 타입스크립트 사용 시 jsconfig.json 활용
```
{
    "compilerOptions": {
        "strict": true
    },
    "include": [
        "src/**/*"
    ]
}
```

위와 같이 설정한 후 타입스크립트를 적용하면
```
const x = null
```
와 같은 코드를 작성할 경우에 `"strict": true` 로 인해 오류를 발생시킨다.


프로젝트마다 필요한 미세한 설정들을 jsconfig 에 설정하여 활용할 수 있음