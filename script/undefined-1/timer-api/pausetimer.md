# pauseTimer()

### 정의

> ### 호출 시 타이머를 일시정지합니다.
>
> * 타이머를 일시 정지합니다.
> * resumeTimer()로 타이머를 정지된 시점부터 이어서 시작할 수 있습니다.



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
    })
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-19_오후_5_36_30_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>

