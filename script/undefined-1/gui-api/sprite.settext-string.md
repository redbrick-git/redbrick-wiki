# sprite.setText(string)

### 정의

> ### GUI의 innertext를 지정한 문자열로 변경합니다.
>
> * **string**\
>   innertext로 사용할 문자열을 입력합니다.
> *   **object**
>
>     *   array
>
>         GUI 텍스트 변경이 반영될 player 정보를 담는 배열입니다.
>
>



### 예시

```javascript
const board = getObject("board_at_c(c78)")

// single project
function OnJoinPlayer(player) {
    startTimer()
    onSecond(1, function() {
        board.setText(floor(getTimer()))
    })
}

// multiplay project case 1
function OnJoinPlayer(player) {
    startTimer()
    onSecond(1, function() {
        // target player의 board GUI 텍스트를 변경합니다.
        board.setText(floor(getTimer()), {target: [player]})
    })
}

// multiplay project case 2
function OnJoinPlayer(player) {
    startTimer()
    onSecond(1, function() {
        // 모든 player의 board GUI 텍스트를 변경합니다.
        board.setText(floor(getTimer()))
    })
}
```

<figure><img src="../../../.gitbook/assets/starTimer_getTimer_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>

