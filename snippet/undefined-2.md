# 밟으면 사라지는 징검다리 만들기

### 1. 원하는 곳에 오브젝트 놓기

징검다리가 사라져야 할 부분에 오브젝트를 놓은 후 title명을 변경합니다.

<figure><img src="../.gitbook/assets/사라져야 할 징검다리-2.png" alt=""><figcaption><p>징검다리 놓기</p></figcaption></figure>

### 2. 코드 입력하기

#### 예시

```javascript
const falsebox =[];
let player = getObject("player")
for(let i = 0; i < 5; i++)
    falsebox[i] = getObject("falsebox_0" + (i + 1));

falsebox.forEach(boxes => {
    player.onCollide(boxes, function() {
        boxes.kill()
        wait(1)
        boxes.revive()
    })   
})
```

<figure><img src="../.gitbook/assets/밟으면 사라지는 징검다리 만들기.gif" alt=""><figcaption><p>실행화면</p></figcaption></figure>
