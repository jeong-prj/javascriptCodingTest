# 제일 작은 수 제거하기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12935
## solution.js
### First
```
function solution(arr) {  
    if(arr.length>1){
        //같은 작은 숫자가 여러개일 경우 ...arr로 처리
        arr.splice(arr.indexOf(Math.min(...arr)),1);
        return arr;
    }else{
        return [-1];
    }
}
```
### Second
```

```
