# 체육복
## problem link
https://programmers.co.kr/learn/courses/30/lessons/42748
## solution.js
### First
```
function solution(array, commands) {
    var answer = [];
    
    commands.forEach(function(arr) {
        let sortedArray = array.slice(arr[0]-1,arr[1]).sort(function(a,b){
            return a-b;
        });
        answer.push(sortedArray[arr[2]-1]);                 
    });
    return answer;
}
```
### Second
```
function solution(array, commands) {
    var answer = [];

    answer = commands.map(a=>{//map 이용
        return array.slice(a[0]-1,a[1]).sort((b,c)=>b-c)[a[2]-1]; //한 줄로
    })
    return answer;
}
```
