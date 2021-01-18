크레인 인형뽑기 
@problem link
https://programmers.co.kr/learn/courses/30/lessons/64061

@solution.js
function solution(board, moves) {
    var answer = 0;
    let basket = [];
    for (let i=0;i<moves.length;i++){
        let pick = moves[i]-1;
        for (let j=0;j<board.length;j++){
            if(board[j][pick]>0){
                basket.push(board[j][pick]);
                board[j][pick] = 0;
                let basketLen = basket.length;
                if(basketLen>1){
                    if(basket[basketLen-2]==basket[basketLen-1]){
                        answer += 2;
                        basket.pop();
                        basket.pop();
                        
                    }
                }
                break;
            }

        }
    }
    return answer;
}
