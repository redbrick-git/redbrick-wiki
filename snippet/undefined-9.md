# 정해진 목숨 만들기

### 1. 원하는 GUI 선택

목숨 카운트를 띄우고자 하는 GUI를 선택합니다.

<figure><img src="../.gitbook/assets/정해진 목숨 만들기.png" alt=""><figcaption><p>원하는 GUI 선택</p></figcaption></figure>

### 2. 코드 입력하기

#### 예시&#x20;

```javascript
const board = getObject("ballstopcle_tab_a(3ae)")
const limit = { y : -5 }
let player = getObject("player")
let die = 3;

setInterval(()=> {
   const pl_pos = player.getPosition();
   if(pl_pos.y < limit.y){
    player.spawn()
    die--; 
    board.setText(`남은 목숨 : ${die}`)
    
    if (die == 0){
    board.setText("GAME OVER")
    enableKeyControl(false)
}
   }
})

function Setup() {
    board.setText(`남은 목숨 : ${die}`)
}
```

<figure><img src="../.gitbook/assets/정해진 목숨 만들기.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
