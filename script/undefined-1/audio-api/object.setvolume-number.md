# object.setVolume(number)

### 정의

> ### 오디오 오브젝트의 음량을 설정합니다.
>
> * **number**\
>   음량을 입력합니다.\
>   number가 작을 수록 작게 들립니다.



### 예시

```javascript
const sound = getObject("dreamy(7e3)")

onKeyDown("KeyZ", function() {
    sound.setVolume(0.1)
})
```
