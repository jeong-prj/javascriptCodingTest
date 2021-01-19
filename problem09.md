# 가운데 글자 가져오기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12903
## solution.js
### First
```
function solution(s) {
    var answer = '';
    
    if((s.length%2) === 0){
        answer = s.slice(s.length/2-1, s.length/2+1);
    }else{
        answer = s.slice(s.length/2, s.length/2+1);
    }
    
    return answer;
}
```
### Second
```
function solution(s) {
  //substring(start, end): 문자열을 추출하는 함수
  //Math.floor() : 소수점 이하를 버림
  //Math.ceil() : 소수점 이하를 올림
  return s.substring(Math.ceil(s.length/2)-1,Math.floor(s.length/2)+1);
}
```
