# 키패드 누르기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/67256
## solution.js
### First
```
function solution(numbers, hand) {
    var answer = '';
    let locOfL = '10';
    let locOfR = '12';
    
    numbers.forEach(function(a){
        //console.log(locOfL,locOfR);
        if(a===1||a===4||a===7){
            locOfL = a; answer+='L';
        }else if(a===3||a===6||a===9){
            locOfR = a; answer+='R';
        }else {
            if(a === 0){
                a = 11;
            }
            const distL = Math.abs(locOfL-a)%3 + Math.floor((Math.abs(locOfL-a)/3));
            const distR = Math.abs(locOfR-a)%3 + Math.floor((Math.abs(locOfR-a)/3));;
            
            if(distL===distR){
                if(hand === 'right'){
                    answer+= 'R'; locOfR = a;
                }
                if(hand === 'left'){
                    answer+= 'L'; locOfL = a;
                }
            }
            if(distL>distR){
                answer+='R'; locOfR = a;
            }
            if(distL<distR){
                answer+='L'; locOfL = a;
            }
        }
    });

    return answer;
}
```
### Second
```

```
