# 자연수 뒤짚어 배열로 만들기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12932
## solution.js
### First
```
function solution(n) {
    var answer = [];
    
    n.toString()
     .split('')
     .reverse()
     .forEach(a=> answer.push(Number(a)));
    
    return answer;
}
```
### Second
```
function solution(n) {
    var answer = [];

    do {
        answer.push(n%10);
        n = Math.floor(n/10);
    } while (n>0);

    return answer;
}
```
