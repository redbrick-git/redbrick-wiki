# sprite.setTextSize(number)

### 정의

> ### GUI의 innertext의 크기를 지정한 값으로 변경합니다.
>
> * **number**\
>   글자 크기를 입력합니다.
> * **object**
>   *   array
>
>       GUI 텍스트 사이즈 변경이 반영될 player 정보를 담는 배열입니다.



### 예시

```javascript
const board = getObject("board_at_c(c02)")
let size = 10

onClickEmpty(function () {
    size++
    board.setText(size)
    board.setTextSize(size)
})

// multiplay project case 1
function OnJoinPlayer(player) {
    onSecond(1, function() {
        // target player의 board GUI 텍스트를 변경합니다.
        board.setTextSize(10, {target: [player]})
    })
}

// multiplay project case 2
function OnJoinPlayer(player) {
    onSecond(1, function() {
        // 모든 player의 board GUI 텍스트를 변경합니다.
        board.setTextSize(7)
    })
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오전_11_50_35_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
