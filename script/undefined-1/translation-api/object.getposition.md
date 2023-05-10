---
description: 'return : object'
---

# object.getPosition()

### 정의

> ### 호출한 오브젝트의 위치를 반환합니다.



### 예시

```javascript
const tree = getObject("nature_minitree1_006(e3c)")
const board = getObject("board_at_c(9c9)")

board.setText(tree.getPosition().x+", "+tree.getPosition().y+", "+tree.getPosition().z)

onKeyDown("KeyZ", function() {
    tree.goX(20)
    board.setText(tree.getPosition().x+", "+tree.getPosition().y+", "+tree.getPosition().z)
})
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_9_09_04_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
