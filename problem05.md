# 체육복
## problem link
https://programmers.co.kr/learn/courses/30/lessons/42862?language=javascript#
## solution.js
### Fisrt   
```
function solution(n, lost, reserve) {
    var answer = 0;
    let student = Array(n).fill(1);//체육복이 다 있는 상태
    
    lost.forEach(function(l){//체육복 도난
       student[l-1]-=1; 
    });
    reserve.forEach(function(r){//체육복 여벌
       student[r-1]+=1; 
    });
    reserve.forEach(function(r){
        let i = r-1;
        if(student[i]>1){//체육복이 2개 있는 학생들일 때
            if(r===n){
                if(student[i-1]===0){
                   student[i-1]+=1; 
                }
            }else if(i===0){
                if(student[i+1]===0){
                    student[i+1]+=1;
                }
            }else if(i>0&&i<n-1){
                if(student[i-1]===0){
                    student[i-1]+=1;
                }else if(student[i+1]===0){
                    student[i+1]+=1;
                }
            }
        }
    });
    student.forEach(function(i){
        if(i>0){
            answer+=1;
        }
    });
    return answer;
}
```
### Second
```

```
