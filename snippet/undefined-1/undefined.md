# 아이템 획득 시 화면에 카운트되게 만들기

### 1. 원하는 GUI 선택

왼쪽 위 + 버튼 클릭 -> GUI 클릭 -> 원하는 GUI 선택합니다.

<figure><img src="../../.gitbook/assets/아이템획득 후 카운트.png" alt=""><figcaption><p>GUI 선택</p></figcaption></figure>

### 2. 코드 입력하기

#### 예시

```javascript
const coin1 = getObject("coin_01")
const coin2 = getObject("coin_02")
const coin3 = getObject("coin_03")
const showpoint = getObject("board_ao_f(dc8)")
let player = getObject("player")
let coinpoint = 0;

coin1.onCollide(player, function() {
    coinpoint = coinpoint + 1
    coin1.kill()
    showpoint.setText(`모은 코인의 개수 : ${coinpoint} / 3 `)
})
coin2.onCollide(player, function() {
    coinpoint = coinpoint + 1
    coin2.kill()
    showpoint.setText(`모은 코인의 개수 : ${coinpoint} / 3 `)
})
coin3.onCollide(player, function() {
    coinpoint = coinpoint + 1
    coin3.kill()
    showpoint.setText(`모은 코인의 개수 : ${coinpoint} / 3 `)
})

function Setup() {
    showpoint.setText(`모은 코인의 개수 : ${coinpoint} / 3 `)
}
```

#### 예시 2

```javascript
const showpoint = getObject("board_ao_f(dc8)")
let player = getObject("player")
let coinpoint = 0;
const coin = [];
for(let i = 0; i < 3; i++)
    coin[i] = getObject("coin_0" + (i + 1));
    
coin.forEach(coins => {
    player.onCollide(coins, function() {
        coins.kill()
        coinpoint = coinpoint + 1
        showpoint.setText(`모은 코인의 개수 : ${coinpoint} / 3 `)
    })
})

function Setup() {
    showpoint.setText(`모은 코인의 개수 : ${coinpoint} / 3 `)
}
```

<figure><img src="../../.gitbook/assets/아이템획득 카운트.gif" alt=""><figcaption><p>실행화면 </p></figcaption></figure>

