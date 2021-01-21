# 문자열 다루기 기본
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12918
## solution.js
### First
```
function solution(s) {
    return s.length===4||s.length===6 ? !/[\D]/.test(s) : false;
}
```
### Second
```
function solution(s){
  var regex = /^\d{6}$|^\d{4}$/;//정규식으로 문자의 길이도 표현할 수 있다
  return regex.test(s);
}
```
