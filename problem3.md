# 완주하지 못한 선수
## problem link
https://programmers.co.kr/learn/courses/30/lessons/42576   

## solution.js
```
function solution(participant, completion) {
    let newList = completion.reduce((node, index)=>{
        node[index] = (node[index]) ? (node[index]+1) : 1;
        return node;
    },{});
    return participant.find((index) => {
        if(newList[index]){
            newList[index] -= 1;
        } else {
            return true;
        }
    });
}
```
