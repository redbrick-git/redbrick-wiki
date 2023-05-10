# 게임 시작할 때 Start버튼을 누르지 않으면 움직이지 못하게 만들기

#### 예시

```javascript
const startbtn = getObject("casual_a_button_d(dc0)")

function Setup () {
    enableKeyControl(false)
    startbtn.onClick(function() {
    enableKeyControl(true)
    startbtn.hide()
})
}
```

<figure><img src="../../.gitbook/assets/start버튼 눌러야 출발.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
