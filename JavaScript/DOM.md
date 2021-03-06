# DOM 접근 방법

## 요소 1개를 찾기 위한 방법
- document.getElementById() : id 어트리뷰트 값으로 요소 1개를 찾을때 사용한다. 여러개인 경우는 가장 처음에 선택된 요소를 가져온다.
- document.querySelector() : 선택하려는 id값 class값과 같이 css에 적용되어있는 요소 1개를 가져온다. 이 접근 방식 또한 여러개인 경우는 가장 처음에 선택된 요소를 가져온다.

## 요소 여러개 가져오는 방법
- document.getElementsByClasssName() : class 값으로 해당하는 요소를 모두 반환하며 ()안에 여러 개의 class 값을 넣고 싶은 경우 공백으로 구분지어 준다.
- document.querySelectorAll() : 선택하려는 id 또는 class 값과 같이 css에 적용되어있는 값으로 해당하는 모든 요소를 가져온다.

## 요소 탐색
- parentNode : 가져온 요소의 부모 노드를 탐색
- firstChild : 첫 번째 자식 노드를 탐색
- lastChild : 마지막 자식 노드를 탐색
