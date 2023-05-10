# startTimer()

### 정의

> ### 호출 시 타이머를 시작합니다.
>
> * 초(second) 기준의 타이머를 시작합니다.
> * startTimer()로 타이머를 시작한 이후, 다양한 Timer API를 활용할 수 있습니다.



### 예시

```javascript
const board = getObject("board_at_c(c78)")

function OnJoinPlayer(player) {
    startTimer()
    onSecond(1, function() {
        board.setText(floor(getTimer()), {target: [player]})
    })
}
```

<figure><img src="../../../.gitbook/assets/starTimer_getTimer_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>

