# 모의고사   
## Problem link   
https://programmers.co.kr/learn/courses/30/lessons/42840   
## Solution.js   
### First
```
function solution(answers) {
    var answer = [];
    
    const person1 = [1,2,3,4,5];
    const person2 = [2,1,2,3,2,4,2,5];
    const person3 = [3,3,1,1,2,2,4,4,5,5];
    
    let score = {'p1':0,'p2':0,'p3':0};
    //정답이 맞으면 점수 더하기
    for(let i = 0;i < answers.length;i++){
        if(answers[i]===person1[i%5]){
            score['p1']+=1;
        }
        if(answers[i]===person2[i%8]){
            score['p2']+=1;
        }
        if(answers[i]===person3[i%10]){
            score['p3']+=1;
        }
    }
    //다른 점수와 같거나 크면 답에 추가
    if(score['p1']>=score['p2']&&score['p1']>=score['p3']){
        answer.push(1);
    }
    if(score['p2']>=score['p1']&&score['p2']>=score['p3']){
        answer.push(2);
    }
    if(score['p3']>=score['p1']&&score['p3']>=score['p2']){
        answer.push(3);
    }
    
    return answer;
}
```
