# object.setPlaybackRate(number)

### 정의

> ### 오디오 오브젝트의 음원 재생 속도를 설정합니다.
>
> * **number**\
>   재생 속도를 입력합니다. (배속)\
>   기본 재생 속도는 1입니다.



### 예시

```javascript
const sound = getObject("dreamy(7e3)")

onKeyDown("KeyZ", function() {
    sound.setPlaybackRate(1.5) //음원을 1.5배속 재생합니다.
})
```
