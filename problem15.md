# 문자열 내 p와 y의 개수
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12917
## solution.js
### First
```
function solution(s) {
    return [...s].sort().reverse().join('');
}
```
### Second
```
function solution(s) {
  return s
    .split("")
    .sort()
    .reverse()
    .join("");
}
```
