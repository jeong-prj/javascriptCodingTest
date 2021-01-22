# 최대공약수와 최대공배수
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12940
## solution.js
### First
```
function solution(n, m) {
    var answer = [];
    
    answer.push(gcd(n,m));
    answer.push(n*m/answer[0]);
    
    return answer;
}
        
function gcd(a, b){
    if(b===0) return a;
    else return gcd(b, a%b);
}

```
### Second
```
function gcd(a, b) {return b ? greatestCommonDivisor(b, a % b) : Math.abs(a);}
function lcm(a, b) {return (a * b) / greatestCommonDivisor(a, b);}
```
