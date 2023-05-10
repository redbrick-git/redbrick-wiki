# sprite.setScale(x, y, option)

### 정의

> ### GUI의 크기를 지정한 x, y값으로 변경합니다.
>
> **x**
>
> * x축 크기를 입력합니다.
>
> **y**
>
> * y축 크기를 입력합니다.
>
> **object**
>
> *   array
>
>     player를 담는 배열입니다.



### 예시

```javascript
const board = getObject("board_at_c(c02)")

// singleplay project
function OnJoinPlayer(player) {
	onKeyDown("KeyZ", function() {
	    board.setScale(1000, 400)
	})
	
	onKeyUp("KeyZ", function() {
	    board.setScale(500, 200)
	})
}

// multiplay project
function OnJoinPlayer(player) {
	onKeyDown("KeyZ", function(player) {
	    board.setScale(1000, 400, {target: [player]})
	})
	
	onKeyUp("KeyZ", function(player) {
	    board.setScale(500, 200, {target: [player]})
	})
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_1_22_18_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
