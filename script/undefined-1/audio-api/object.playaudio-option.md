# object.playAudio(option)

### 정의

> ### 오디오 오브젝트의 음원을 시작(pause되었다면 멈춘 부분부터 시작)합니다.
>
> * 오디오 오브젝트를 사전에 추가한 이후 사용할 수 있습니다.



### 예시

```javascript
const tree = getObject("nature_minitree1_006(c3e)")
const sound = getObject("draw.mp3(3b1)")

// singleplay project
tree.onCollide("player", function() {
    sound.playAudio() 
})

// multiplay project
tree.onCollide("player", function() {
    sound.playAudio({target : [player]}) 
})
```
