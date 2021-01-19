# 나누어 떨어지는 숫자 배열
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12910
## solution.js
### First
```
function solution(arr, divisor) {// filter를 써보자는 생각으로 작성했지만 실행시간이 너무 많이 걸린다
    let answer = arr.filter(a => (a%divisor)===0).sort((a,b)=>a-b);
    return answer.length ? answer:[-1];
}
```
### Second
```
function solution(arr, divisor) {//filter가 없는 코드 시간은 비슷하다
    var answer = [];

    for(var i = 0; i < arr.length; ++i) {
        if(arr[i] % divisor == 0) answer.push(arr[i]);
    }

    return answer.length < 1 ? [-1] : answer.sort((a, b) => a - b);
}
```
