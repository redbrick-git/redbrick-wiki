# object.onClick(callback)

### 정의

> ### 오브젝트를 클릭했을 때 콜백 함수를 실행합니다.
>
> * **callback(args)**\
>   오브젝트를 클릭했을 때 실행될 코드를 입력합니다.



### 예시

```javascript
const tree = getObject("nature_minitree1_006(c3e)")

// singleplay project
tree.onClick(function() {
    tree.kill()
})

// multliplay project
tree.onClick(function(target) {
    tree.kill
    // target.doSomething()
})
```
