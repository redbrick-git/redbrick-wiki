# object.stopAudio(option)

### 정의

> ### 오디오 오브젝트의 음원을 정지(처음 부분으로 되돌림)합니다.
>
> * playAudio를 활용하여 다시 재생할 수 있습니다.



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

//트리와 접촉하지 않으면 음악을 정지합니다.
//이후에는 음악을 처음부터 다시 재생합니다.
tree.onCollideEnd("player", function() {
    sound.stopAudio()
})

// multiplay project
tree.onCollide("player", function() {
    sound.playAudio({target: [player]})
})

tree.onCollideEnd("player", function() {
    sound.stopAudio({target: [player]})
})
```
