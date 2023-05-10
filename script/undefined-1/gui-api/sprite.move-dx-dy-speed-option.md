# sprite.move(dx, dy, speed, option)

### 정의

> ### GUI를 지정한 dx, dy 거리만큼 지정한 속도로 이동합니다.
>
>
>
> * **dx**\
>   x축 이동 거리를 입력합니다.
> * **dy**\
>   y축 이동 거리를 입력합니다.
> * **speed**\
>   이동 속도를 입력합니다.
> * option
>   *   array
>
>       player를 담는 배열입니다.



### 예시

```javascript
const board = getObject("board_at_c(c02)")

// singleplay project
function OnJoinPlayer(player) {
    onKeyDown("KeyZ", function() {
        board.move(0, 500, 500)
    })

    onKeyDown("KeyX", function() {
        board.move(0, -500, 500)
    })
}

// multiplay project
function OnJoinPlayer(player) {
    onKeyDown("KeyZ", function(player) {
        board.move(0, 500, 500, {target: [player]})
    })

    onKeyDown("KeyX", function(player) {
        board.move(0, -500, 500, {target: [player]})
    })
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_1_28_38_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
