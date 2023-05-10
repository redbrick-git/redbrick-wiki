# object.changePlayerSpeed(number)

### 정의

> ### 지정한 속도로 캐릭터의 속도를 변경합니다.
>
> * 기본 속도는 1입니다.
> * **number**\
>   변경할 속도를 입력합니다.



### 예시

```javascript
const item = getObject("decoration_cutediamond_005(e48)")

function OnJoinPlayer(player) {
	item.onCollide(player, function() {
	    item.kill()
	    player.changePlayerSpeed(2)
	})
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_11_38_25_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
