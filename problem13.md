# 문자열 내 마음대로 정렬하기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12915
## solution.js
###First
```
function solution(strings, n) {
    var answer = [];

    answer = strings.sort(function(a,b){
        if(a[n]===b[n]){
            return a.localeCompare(b);
        }
        if(a[n]!=b[n]){
            return a[n].localeCompare(b[n]);
        }
    });
    
    return answer;
}
```
### Second
```
function solution(strings, n) {
    return strings.sort((a, b) => {
        const chr1 = a.charAt(n);
        const chr2 = b.charAt(n);

        if (chr1 == chr2) {
            return (a > b) - (a < b);
        } else {
            return (chr1 > chr2) - (chr1 < chr2);
        }
    })
}
```
