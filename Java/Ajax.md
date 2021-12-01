## Ajax 란 ?

- Asynchronous JavaScript and XML 약자
- JavaScript를 이용하여 비동기적으로 서버와 브라우저간의 데이터 교환 통신 방식이다.

## Ajax의 특징
```
1. 페이지 새로고침 없이 서버에 요청
2. 서버로부터 데이터를 받고 작업을 수행
```

### JavaScript를 이용한 Http Request 생성 방법


> 객체 생성
```
<pre>
<code>
var request = new XMLHttpRequest();
</code>
</pre>
```

> 비동기 방식으로 request open, 서버에 요청
```
<pre>
<code>
request.open('GET', 'url 값 입력', true);
</code>
</pre>
```

```
`open(방식, 'url', 동기/비동기)` : 
    방식 : GET or POST
    URL : url 주소 , ex) 'api/v1/main'
    동기/비동기 : true면 비동기, false면 동기

    12.01 추가
    만약, false를 사용하면 Ajax를 사용하지 않겠다는 의미로
    false로 요청하게 되면 서버에서 응답이 오기 전까지 화면에서 다른 행동은 불가능하다.
```

> request 전송, 준비된 요청을 서버에 전달
```
<pre>
<code>
request.send();
</code>
</pre>
```

```
`send()` : 
    open()에 작성된 Ajax를 서버로 요청
    GET 방식을 이용 하는 경우 send() 로 요청
    POST 방식을 이용 하는 경우 send('추가데이터') 로 요청
```

> 요청을 send() 후 서버로부터 응답 확인
```
 
```