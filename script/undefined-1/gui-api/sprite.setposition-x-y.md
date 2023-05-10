# sprite.setPosition(x, y)

### 정의

> ### GUI요소의 위치를 지정한 좌표로 변경합니다.
>
> **x**
>
> * x 좌표를 입력합니다.
>
> **y**
>
> * y 좌표를 입력합니다.
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
	    board.setPosition(-800, 400)
	})
	
	onKeyDown("KeyX", function() {
	    board.setPosition(800, 400)
	})
}

// multiplay project
function OnJoinPlayer(player) {
	onKeyDown("KeyZ", function(player) {
	    board.setPosition(-800, 400, {target: [player]})
	})
	
	onKeyDown("KeyX", function(player) {
	    board.setPosition(800, 400, {target: [player]})
	})
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_12_09_15_AdobeExpress (1).gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
