# 아이템 획득 조건 충족 시 막혀있던 벽이 열리게 만들기

#### 예시

```javascript
const showpoint = getObject("board_ao_f(dc8)")
const door = getObject("furniture_dgdoor_003(cb5)")
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
        if(coinpoint == 3){
            door.moveY(8, 5)
        }
    })
})

function Setup() {
    showpoint.setText(`모은 코인의 개수 : ${coinpoint} / 3 `)
}
```

<figure><img src="../../.gitbook/assets/일정부분 채우면 열리게 만들기.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
