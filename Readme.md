## 프로젝트-이주성
## 22와 가깝게 카드뽑기게임
### 요구사항 정리
클래스 구성

Application : main 메소드 포함

MainMenu :


    gameMain() : do-whlie 문으로 1.게임시작 2.게임종료를 고를 수 있게함
    1.게임시작
    게임시작을 누르면 gamestart()메소드가 실행
    do-while문으로 1.카드뽑기 2.비교하기를 고를 수 있음.
        
        1.카드뽑기를 누르면 FunctionSystem.getCard()가 실행
        카드는 최대 3번까지 뽑을 수 있고 카드뽑기를 누른 횟수만큼 computer도 카드뽑기 추가
    
        2.비교하기를 누르면 FunctionSystem.whoIsWinner()가 실행
        비교하기를 누르면 내가 뽑은 카드들의 합과 computer가 뽑은 카드들의 합 중 22와 더 가까운 합이 승리
        FunctionSystem.whoIsWinner()가 실행 완료 후 gameMain()메소드로 넘어감

    2.게임종료 
    게임종료를 누르면 게임이 종료됨

FunctionSystem :

    getCard() : MainMenu클래스의 gameMain()메소드 1.카드뽑기를 누르면 실행되는 메소드
                카드는 1~10까지 랜덤하게 뽑히며 뽑은 카드들의 합을 구해서 저장
                내가 뽑은 카드 횟수만큼 computer도 카드를 뽑으며 마찬가지로 1~10까지 랜덤하게
                뽑힌 카드들의 합을 구해서 저장
    whoIsWinner() : MainMenu클래스의 gameMain()메소드 2.비교하기를 누르면 실행되는 메소드
                    getCard()로 리턴된 내가 뽑은 카드의 합과 computer가 뽑은 카드의 합을 비교
                    둘 중 22에 더 가까운 합이 승리
                    승리를 축하하는 출력문이 나옴