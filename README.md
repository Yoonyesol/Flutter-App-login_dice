Flutter-App-login_dice
==================

📱안드로이드 스튜디오를 이용하여 플러터 주사위 어플 제작
-------------------

## 🏡로그인 기능
* `controller`를 이용하여 `TextField`에서 입력받은 정보를 받아오기
* `FocusScope.of(context).unfocus()`를 이용해 텍스트 필드 외부 영역을 터치할 시 키보드가 사라지도록 처리
* if문을 이용해 사용자가 텍스트 필드에 *id: dice / pw: 1234* 이외의 값을 입력할 경우 로그인 할 수 없도록 처리
* 사용자가 지정된 id, pw값을 입력한 경우 dice 페이지로 넘어가도록 `Navigator`를 이용한 페이징 처리
```kotlin
Navigator.push(context, 
    MaterialPageRoute(builder: (BuildContext context) => Dice()));
```


<br/><br/>
## 🎲주사위 굴리기 기능
* `Column`과 `Row` 위젯을 이용하여 주사위 이미지 배치
* 왼쪽 주사위와 오른쪽 주사위에 랜덤번호를 부여하여 랜덤으로 주사위 이미지가 바뀌게 처리
```
setState(() {
    leftDice = Random().nextInt(6) + 1;
    rightDice = Random().nextInt(6) + 1;
});
```
```
Image.asset('image/dice$leftDice.png')
```
```
Image.asset('image/dice$rightDice.png')
```
* 부여된 랜덤번호를 토스트 메시지로 출력처리


<br/><br/>
## ☺새로 학습한 내용
* `TextField`의 내용을 `Controller`로 처리하는 방법을 익혔다.
* `Column`과 `Row` 위젯에서의 `mainAxisAlignment:MainAxisAlignment.center` 사용법을 다시 한 번 체득했다. 
* 이미지 파일명을 변수처리하여 상태값을 변화시키는 방법을 알게 되었다. (`$`기호 사용법)
* `pubspec.yaml`파일에 `fluttertoast`라이브러리를 등록하면서 발생한 오류를 공식문서를 찾아보며 해결하였다.
* 추가로 git 사용법, mark down 사용법도 익혀가는 중



</br></br>
## 코드 원문 출처
<코딩셰프> 주사위 만들기 강좌 </br>
<https://www.youtube.com/playlist?list=PLQt_pzi-LLfoOpp3b-pnnLXgYpiFEftLB> 


