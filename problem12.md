# 두 정수 사이의 합
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12912
## solution.js
### First
```
function solution(a, b) {
    var answer = 0;
    if(a>b){//최대한 쉽게 푼 코드
        let tmp = 0;
        tmp = a;
        a = b;
        b = tmp;
    }
    for(a;a<=b;a++){
        answer+=a;
    }
    
    return answer;
}
```
### Second
```
function solution(a, b){//단시간 안에 해결되는 코드 머리를 써야 코드도 간단하다 
    return (a+b)*(Math.abs(b-a)+1)/2;
}
```
