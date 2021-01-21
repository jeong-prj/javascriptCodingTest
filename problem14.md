# 문자열 내 p와 y의 개수
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12916
## solution.js
### First
```
function solution(s){
    const lowerS = s.toLowerCase();
    if((lowerS.match(/y/g)||[]).length===(lowerS.match(/p/g)||[]).length){
        return true;
    }else {
        return false;
    }
}
```
### Second
```
function solution(s){
    return s.toUpperCase().split("P").length === s.toUpperCase().split("Y").length;
}
```
