# object.pauseAudio(option)

### 정의

> ### 오디오 오브젝트의 음원을 일시정지합니다.
>
> * playAudio를 활용하여 이어서 재생할 수 있습니다.



### 예시

```javascript
const tree = getObject("nature_minitree1_006(c3e)")
const sound = getObject("dreamy(7e3)")

function Setup() {
    stopAllSound()
}

// singleplay project
tree.onCollide("player", function() {
    sound.playAudio()
})

//트리와 접촉하지 않으면 음악을 일시 정지합니다.
tree.onCollideEnd("player", function() {
    sound.pauseAudio()
})

// multiplay project
tree.onCollide("player", function() {
    sound.playAudio({target: [player]})
})

tree.onCollideEnd("player", function() {
    sound.pauseAudio({target: [player]})
})

```
