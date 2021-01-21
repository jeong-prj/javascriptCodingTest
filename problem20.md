# 문자열을 정수로 바꾸기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12925
## solution.js
### First
```
function solution(s) {
    return Number(s);//javascript는 문자열을 정수로 바꿀 때 - 기호도 인식한다
}
```
### Second
```
function solution(s){
  return str/1; //사칙연산을 통해 자료형 변환?? 숫자라고 인식하게
  }
```
