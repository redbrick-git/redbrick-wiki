# object.takeShadow(boolean)

### 정의

> ### 오브젝트 표면에 그림자가 드리워지는지 여부를 조정합니다.
>
> * 레드브릭 스튜디오의 빛(light)에 따라 그림자가 생성됩니다.
> *   **boolean**
>
>     true : 그림자가 드리워집니다.
>
>     false : 그림자가 드리워지지 않습니다.



### 예시

```javascript
const tree = getObject("nature_palmtree_001(cdf)")

function Setup() {
    tree.takeShadow(true)
}
```

