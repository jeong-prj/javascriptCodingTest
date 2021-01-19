# 2016년
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12901
## solution.js
```
function solution(a, b) {
    var answer = '';
    const day = ['THU','FRI', 'SAT', 'SUN', 'MON', 'TUE', 'WED'];
    const days = [31,29,31,30,31,30,31,31,30,31,30,31];
    let sumOfDay = 0;
    
    for(let i=0;i<a-1;i++){
        sumOfDay += days[i];
    }
    answer= day[(sumOfDay + b)%7];
    
    return answer;
}
```
