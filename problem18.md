# 소수 찾기
## problem link

## solution.js
### First
```
function solution(n) { // 시간초과로 통과하지 못했다
    var answer = 0;
    for(let i = 2; i <=n;i++){
        for(let j = 2; j <= i; j++){
            if(i===j){
                    answer+=1;
                    break;
                }
            if(i%j===0){
                break;
            }
        }
    }
    return answer;
}
```
### Second
```
function solution(n) {//에라토스테네스의 체를 이용한 방법이란다
  //소수들의 배수를 제거시키면서 소수를 찾는다
  const answer = new Array(n).fill(true);
  answer[0] = false;
  for (let i = 2; i ** 2 <= n; i++) {
    if (answer[i - 1] === true) {
      for (let j = i ** 2; j <= n; j += i) {
        answer[j - 1] = false;
      }
    }
  }
  return answer.filter((e) => e).length;
}
```
