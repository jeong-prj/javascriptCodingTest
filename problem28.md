# 정수 제곱근 판별
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12934
## solution.js
### First
```
function solution(n) {
    var answer = 0;
    
    answer = (Math.sqrt(n))%1===0 ? (Math.sqrt(n)+1)**2: -1;
    
    return answer;
}
```
### Second
```

```
