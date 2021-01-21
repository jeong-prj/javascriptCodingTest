# 수박수박수박수박수박수?
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12922
## solution.js
### First
```
function solution(n) {   
    let answer = '';
    const pattern = ['수','박']
    
    for(let i = 0;i<n;i++){
        answer += pattern[i%2];
    }
    
    return answer;
}
```

