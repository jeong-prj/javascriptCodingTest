# 같은 숫자는 싫어
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12906
## solution.js
### First
```
function solution(arr){
    var answer = [];
    
    for(var i = 0; i < arr.length; i++){//for문보다 forEach문이 느리다고 한다
        if(arr[i] !== arr[i + 1]){
           answer.push(arr[i]);
        }        
    }
    
    return answer;
}
```
### Second
```
function solution(arr){
    return arr.filter((val,index) => val != arr[index+1]); //filter를 이용한 풀이 방법
}
```
