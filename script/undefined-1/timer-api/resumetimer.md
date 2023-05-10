# resumeTimer()

### 정의

> ### 호출 시 타이머를 멈춘 시점부터 시작합니다.
>
> * 타이머를 이어서 시작 합니다.
> * pauseTimer()로 정지된 타이머를 이어서 시작할 수 있습니다.



### 예시

```javascript
const board = getObject("board_at_c(c78)")
const item = getObject("decoration_cutediamond_001(c32)")

function OnJoinPlayer(player) {
    startTimer()
    onSecond(1, function() {
        board.setText(floor(getTimer()), {target: [player]})
    })
    
    item.onCollide(player, function() {
        item.kill()
        pauseTimer()
        wait(3)
        resumeTimer()
        item.revive()
    })
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-19_오후_5_41_25_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
