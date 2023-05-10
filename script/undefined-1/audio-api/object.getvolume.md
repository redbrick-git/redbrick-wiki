---
description: 'return : number'
---

# object.getVolume()

### 정의

> ### 오디오 오브젝트의 현재 음량을 반환합니다.



### 예시

```javascript
const sound = getObject("dreamy(7e3)")

onKeyDown("KeyZ", function() {
    console.log(sound.getVolume()) //콘솔 창에 현재 음량을 출력합니다.
})
```
