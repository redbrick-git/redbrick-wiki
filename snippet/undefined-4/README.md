# 특정 조건에서 캐릭터 속도 변화주기

### 1. 원하는 곳에 오브젝트 놓기&#x20;

&#x20;원하는 곳에 오브젝트를 놓습니다.

<figure><img src="../../.gitbook/assets/캐릭터 속도 변화주기.png" alt=""><figcaption><p>원하는 오브젝트 선택</p></figcaption></figure>

### 2. 코드 입력하기

#### 예시

```javascript
const speedbox = getObject("decoration_randombox_001(ddd)")
let player = getObject("player")
speedbox.onCollide(player, function() {
    speedbox.kill()
    player.changePlayerSpeed(2)
})
```

<figure><img src="../../.gitbook/assets/특정 조건에서 캐릭터 속도 변화주기.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
