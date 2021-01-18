# 두 개 뽑아서 더하기   
## @problem link   
https://programmers.co.kr/learn/courses/30/lessons/68644     
   
## @solution.js   
### First
<pre>
<code>
function solution(numbers) {
    var answer = [];
    console.log(numbers);
    for(let i=0;i<numbers.length;i++){
        for(let j=0;j<i;j++){
            let sum =numbers[i]+numbers[j];
            if(!answer.includes(sum)){
                answer.push(sum);
            }
        }
    }
    answer.sort(function(a,b){
        return a-b;
    });
    return answer;
}
</code>
</pre>
### Second   
<pre>
<code>
function solution(numbers) {
    var tmp = [];
    console.log(numbers);
    for(let i=0;i<numbers.length;i++){
        for(let j=0;j<i;j++){
            tmp.push(numbers[i]+numbers[j]);
        }
    }
    let answer = [...new Set(tmp)];//중복된 item을 제거
    answer.sort(function(a,b){
        return a-b;//배열을 오름차순으로 정렬
    });
    return answer;
}
</code>
</pre>
