# enableKeyControl(boolean)

### 정의

> ### 키입력 이벤트를 제거/복구합니다.
>
> 아바타 조작을 포함한, 모든 키 입력 이벤트를 사용 가능 혹은 불가능하게 합니다.
>
> * **boolean**\
>   true : 키 입력 이벤트 사용이 가능합니다.\
>   false : 키 입력 이벤트 사용이 불가능합니다. 아바타 조작도 불가능합니다.
> *   **option**
>
>     멀티플레이의 경우 사용합니다. 키입력 이벤트를 제거/복구할 플레이어를 배열에 담아 전달합니다.



### 예시

```javascript
const sphere = getObject("SPHERE(516)")

sphere.onClick(function() {
    enableKeyControl(false)
})

// multiplay
sphere.onClick(function() {
    // player1, player2의 키입력 이벤트가 제거됩니다.
    enableKeyControl(false, {target: [player1, player2]})
})
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-14_오후_10_50_29_AdobeExpress (1).gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
