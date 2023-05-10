---
description: 'return : object'
---

# getMousePosition()

### 정의

> ### 호출한 시점의 마우스 포인터 좌표를 반환합니다.
>
> <mark style="color:red;">(주의) 멀티플레이 프로젝트에서는 동작하지 않습니다!</mark>
>
> * X축,Y축 좌표가 객체 형태로 반환됩니다.
> * getMousetPosition().x로 X좌표에 접근 가능합니다.
> * getMousetPosition().y로 Y좌표에 접근 가능합니다.



### 예시

```javascript
const board = getObject("board_at_c(690)")

onClickEmpty(function () {
    board.setText("X: "+getMousePosition().x+"\n"+"Y: "+getMousePosition().y)
})
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-14_오후_10_38_26_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
