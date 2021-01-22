# 자릿수 더하기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12931
## solution.js
### First
```
function solution(n)
{
    var answer = 0;

    [...n.toString()].forEach(a=>answer+=a/1);

    return answer;
}
```
### Second
```
unction solution(n){
    // split을 이용
    return (n+"").split("").reduce((acc, curr) => acc + parseInt(curr), 0)
}
```
