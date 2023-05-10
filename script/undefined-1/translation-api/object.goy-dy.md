# object.goY(dy)

### 정의

> ### 오브젝트를 y축으로 지정한 만큼 바로 이동합니다.
>
> * **dy**\
>   y축 이동량을 입력합니다.



### 예시

```javascript
const tree = getObject("nature_minitree1_006(e3c)")

onKeyDown("KeyZ", function() {
    tree.goY(10)
})
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_8_51_19_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
