# 점프해서 아이템 획득하기

### 1. 원하는 곳에 오브젝트 놓기

원하는 곳에 아이템을 놓습니다.&#x20;

{% hint style="info" %}
아이템이 많아지면 정리하기 힘들기 때문에 title을 정리해주면 좋습니다.
{% endhint %}

<figure><img src="../../.gitbook/assets/title 조정.png" alt=""><figcaption><p>아이템 위치 조정</p></figcaption></figure>

### 2. 코드 입력하기

#### 예시

```javascript
const coin1 = getObject("coin_01");
const coin2 = getObject("coin_02");
const coin3 = getObject("coin_03");
let player = getObject("player");

coin1.onCollide(player, function() {
    coin1.kill()
})
coin2.onCollide(player, function() {
    coin2.kill()
})
coin3.onCollide(player, function() {
    coin3.kill()
})
```

#### 예시 2

```javascript
let player = getObject("player")
const coin = [];
for(let i = 0; i < 3; i++)
    coin[i] = getObject("coin_0" + (i + 1));
    
coin.forEach(coins => {
    player.onCollide(coins, function() {
        coins.kill()
    })
})
```

<figure><img src="../../.gitbook/assets/아이템 획득하기.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
