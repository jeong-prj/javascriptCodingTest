# 3진법 뒤집기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/68935
## solution.js
### First
```
function solution(n) {
    var answer = 0;
    let nIn3 = [];
    while(1){
        if(n<3){
            nIn3.push(n);
            break;
        }else{
            nIn3.push(n%3);
            n = parseInt(n / 3);
        }
    }
    nIn3.reverse().forEach(function(a, index){
        answer += a*(3**index);
    });

    return answer;
}
```
### Second
```
function solution(n) {
  n = n.toString(3).split('').reverse().join('') //toString 으로 간단하게 진법으로 바꿨다
  return parseInt(n, 3)//parseInt로 간단하게 10진수로 바꾼다
}
```
