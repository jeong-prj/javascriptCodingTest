# 정수 내림차순으로 배치하기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12933
## solution.js
### First
```
function solution(n) {
    var answer = 0;
    
    answer=[...n.toString()].sort(function(a,b){
        return b/1-a/1;
    })
    
    return answer.join('')/1;
}
```
### Second
```
function solution(n) {
    var nums =[];
    do{
        nums.push(n%10);
        n=Math.floor(n/10);
    } while(n>0)

    return nums.sort((a,b)=>b-a).join('')*1;
}
```
