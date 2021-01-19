# 모의고사   
## problem link   
https://programmers.co.kr/learn/courses/30/lessons/42840   
## solution.js   
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
### Second   
다른 사람의 풀이 Math.max , filter
```
function solution(answers) {
    let answer = [];
    const a1 = [1, 2, 3, 4, 5];
    const a2 = [2, 1, 2, 3, 2, 4, 2, 5]
    const a3 = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5];

    const a1c = answers.filter((a,i)=> a === a1[i%a1.length]).length;
    const a2c = answers.filter((a,i)=> a === a2[i%a2.length]).length;
    const a3c = answers.filter((a,i)=> a === a3[i%a3.length]).length;
    var max = Math.max(a1c,a2c,a3c);

    if (a1c === max) {answer.push(1)};
    if (a2c === max) {answer.push(2)};
    if (a3c === max) {answer.push(3)};


    return answer;
}
```
