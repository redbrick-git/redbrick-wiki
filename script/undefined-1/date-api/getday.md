---
description: 'return : number'
---

# getDay()

### 정의

> ### 현재 날을 정수로 반환합니다.
>
> * 게임이 실행되는 현재 일자의 날을 반환합니다.



### 예시

```javascript
const board = getObject("board_at_c(c78)")
onSecond(1, function() {
    board.setText(getYear()+"/"+getMonth()+"/"+getDay()+"\n"
    +getHour()+":"+getMinutes()+":"+getSeconds())
})
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-19_오후_8_07_44_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
