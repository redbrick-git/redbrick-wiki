# 반복적으로 움직이는 물체 만들기

### 1. 원하는 오브젝트 포지션 확인

원하는 오브젝트의 포지션을 확인합니다.

<figure><img src="../.gitbook/assets/반복적으로 움직이는 물체.png" alt=""><figcaption><p>포지션 확인</p></figcaption></figure>

### 2. 코드 입력하기

포지션에 맞춰 코드를 입력합니다.

{% hint style="info" %}
delay default 값은 4 ms로 정해져 있다.
{% endhint %}

#### 예시

```javascript
const movebox = getObject("BOX(f7b)")

setInterval(() => {
    const pos = movebox.getPosition();
    if (pos.x >= 15 ) {
        movebox.moveX(-10, 6)
    }
    else if(pos.x <= 5){
        movebox.moveX(10, 6)
    }
})
```

<figure><img src="../.gitbook/assets/반복적으로 움직이는 물체 만들기.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
