# 이상한 문자 만들기
## problem link
https://programmers.co.kr/learn/courses/30/lessons/12930
## solution.js
### First
```
function solution(s) {
    //var answer = '';
    let words = [];
    words = s.split(' ');
    
    words.forEach(function(a,index){
        let word = a.split('')
        for(let i=0;i<a.length;i++){
            word[i] = (i%2)===0 ? word[i].toUpperCase() : word[i].toLowerCase();
        }
        words[index] = word.join('');
    });
    
    return words.join(' ');
}
```
### Second
```
function solution(s) {
  return s.toUpperCase()
          .replace(/(\w)(\w)/g, function(a){return a[0].toUpperCase()+a[1].toLowerCase();});
}
```
