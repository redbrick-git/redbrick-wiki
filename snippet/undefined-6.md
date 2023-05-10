# 게임 종료 시 처음화면으로 돌아가기

### 1. 원하는 GUI 선택

원하는 GUI를 선택합니다.&#x20;

<figure><img src="../.gitbook/assets/게임 종료시 처음화면.png" alt=""><figcaption><p>GUI 선택</p></figcaption></figure>



### 2. 코딩 입력하기

#### 예시

```javascript
let player = getObject("player")

const viclogo = getObject("sf_a_font_e(15f)")
const startbtn = getObject("button_ao_m(ee1)")
const retrybtn = getObject("button_ao_o(456)")
const finish = getObject("BOX(32f)")

finish.onCollide(player, function() {
    enableKeyControl(false)
    viclogo.show()
    wait(2)
    retrybtn.show()
})

retrybtn.onClick(function() {
    viclogo.hide()
    retrybtn.hide()
    startbtn.show()
    player.spawn()
})

function Setup() {
    viclogo.hide()
    retrybtn.hide()
    enableKeyControl(false)
    
    startbtn.onClick(function() {
        enableKeyControl(true)
        startbtn.hide()
    })
}
```

<figure><img src="../.gitbook/assets/게임 종료 시 처음화면.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
