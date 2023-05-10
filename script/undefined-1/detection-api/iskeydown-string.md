---
description: 'return : boolean'
---

# isKeyDown(string)

### 정의

> ### 호출 시점에 특정 키를 누르고 있는지 반환합니다.
>
> <mark style="color:red;">(주의) 멀티플레이 프로젝트에서는 동작하지 않습니다!</mark>
>
> * **string**\
>   Key\[key] 형태로 키를 입력합니다.



### 예시

```javascript
const box = getObject("BOX(356)")

function OnJoinPlayer(player) {
  box.onContact(player, function() {
      if(isKeyDown("KeyZ")){
          box.kill()
      }
  })
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-19_오후_10_39_03_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>

