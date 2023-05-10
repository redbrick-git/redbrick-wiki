# sprite.show()

### 정의

> ### 호출한 GUI요소가 숨겨져 있다면 다시 나오게 합니다.
>
> GUI 요소를 숨기는 hide()와 함께 사용합니다.\
>
>
> **object**
>
> *   array
>
>     player를 담는 배열입니다.





### 예시

```javascript
const board = getObject("board_at_c(c02)")
const menu = getObject("casual_a_button_o(5a5)")
const quit = getObject("button_bd_i_01(7ce)")

// singleplay project
function OnJoinPlayer(player) {
	board.hide()
	quit.hide()
	
	menu.onClick(function() {
	    board.show()
	    quit.show()
	    board.setText("Hello, World!")
	})
	
	quit.onClick(function() {
	    board.hide()
	    quit.hide()
	    board.setText("")
	})
}

// multiplay project
function OnJoinPlayer(player) {
	board.hide({target: [player]})
	quit.hide({target: [player]})
	
	menu.onClick(function(player) {
	    board.show({target: [player]})
	    quit.show({target: [player]})
	    board.setText("Hello, World!", {target: [player]})
	})
	
	quit.onClick(function(player) {
	    board.hide({target: [player]})
	    quit.hide({target: [player]})
	    board.setText("", {target: [player]})
	})
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오전_11_59_07_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
