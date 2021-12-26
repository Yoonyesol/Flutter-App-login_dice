Flutter-App-login_dice
==================

안드로이드 스튜디오를 이용하여 플러터 주사위 어플 제작
-------------------

##로그인 기능
*<pre>controller</pre>를 이용하여 <pre>TextField</pre>에서 입력받은 정보를 받아오기
*<pre>FocusScope.of(context).unfocus()</pre>를 이용해 텍스트 필드 외부 영역을 터치할 시 키보드가 사라지도록 처리
*if문을 이용해 사용자가 텍스트 필드에 *id: dice / pw: 1234* 이외의 값을 입력할 경우 로그인 할 수 없도록 처리
*사용자가 지정된 id, pw값을 입력한 경우 dice 페이지로 넘어가도록 <pre>Navigator</pre>를 이용한 페이징 처리
```kotlin
Navigator.push(context, 
    MaterialPageRoute(builder: (BuildContext context) => Dice()));
```

##주사위 굴리기 기능


