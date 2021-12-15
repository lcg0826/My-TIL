# Object 란 ?

- 자바스크립트는 객체 기반의 언어로, 원시 값을 제외한 함수, 배열 등은 모두 객체이다.
- 객체는 0개 이상의 프로퍼티로 구성된 집합, 프로퍼티는 key : value 구성
    ```
    var std = {
        std_num : 1,
        name : '홍길동',
        age : 22 
    };
    ```
    - 위 std 함수에서 std_num : 1, name : '홍길동', age : 22 는 프로퍼티
    - std_num, name, age는 프로퍼티 key
    - 1, '홍길동', 22는 프로퍼티 value


- 자바스크립트에서 사용할 수 있는 모든 값은 프로퍼티 값이 가능
- 프로퍼티의 값이 함수인 경우는 `메소드` 라고 부른다.
    ```
    var std = {
        std_num : 1,
        name : '홍길동',
        std_grade : 1,
        std_grade_add : function() {
            this.std_grade++;
        }
    };
    '''
    
## 프로퍼티 접근 방법

1. 객체명.프로퍼티키
2. 객체명['프로퍼티키']

- 위에서 생성한 std 객체를 예시로
    ```
    console.log(std.std_num) -> 1
    console.log(std.name) -> 홍길동
    console.log(std.std_grade) -> 1
    ```
    
### 프로퍼티 추가 생성 / 수정 / 삭제 

- 생성
    ```
    var std = {
        std_num : 1,
        name : '홍길동',
        std_grade : 1,
        std_grade_add : function() {
            this.std_grade++;
        }
    };
    
    std.name = '김아무개';
    ```
    
    ```
    console.log(std.name); -> '김아무개'
    ```
    
- 수정
    ```
    var std = {
        std_num : 1,
        name : '김아무개',
        std_grade : 1,
        std_grade_add : function() {
            this.std_grade++;
        }
    };
    
    std.tel = '010-1234-5678';    
    ```
    
    ```
    console.log(std.tel) -> '010-1234-5678;
    ```
    
- 삭제
    ```
    var std = {
        std_num : 1,
        name : '김아무개',
        std_grade : 1,
        tel : '010-1234-5678',
        std_grade_add : function() {
            this.std_grade++;
        }
    };
    
    delete std.tel;
    ```
    
    ```
    var std = {
        std_num : 1,
        name : '김아무개',
        std_grade : 1,
        std_grade_add : function() {
            this.std_grade++;
        }
    };
    ```
