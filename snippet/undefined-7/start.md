# Start버튼 클릭 한 이후부터 타이머가 작동되게 만들기

#### 예시

```javascript
let count = 0;

const startbtn = getObject("casual_a_button_d(dc0)")
const timerboard = getObject("button_bj_e(1fa)")
    
function Setup() {
    enableKeyControl(false)
    startbtn.onClick(function() {
        enableKeyControl(true)
        startbtn.hide()
        
        const startCount = setInterval(() => {
                count++;
                timerboard.setText(count, true)
                }, 1000)
    })
}
```

<figure><img src="../../.gitbook/assets/게임 시작 시 타이머.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
