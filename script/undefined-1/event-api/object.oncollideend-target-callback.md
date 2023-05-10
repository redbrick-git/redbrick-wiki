# object.onCollideEnd(target, callback)

### 정의

> ### 오브젝트에 타겟이 충돌 후 벗어났을 때 콜백 함수가 실행합니다.
>
> * **target**\
>   충돌했는지 판단할 타겟을 입력합니다.\
>   아바타의 경우 player를 입력합니다.
> * **callback(args)**\
>   타겟이 충돌에서 벗어났을 때 실행될 코드를 입력합니다.



### 예시

```javascript
const tile = getObject("decoration_concretetile_001(dcc)")

// singleplay project
function OnJoinPlayer(player) {
	tile.onCollideEnd(player, function() {
	    tile.kill()
	})
}

// multiplay project
function OnJoinPlayer(player) {
	tile.onCollideEnd(player, function(target) {
	    tile.kill()
	    // target.doSomething()
	})

}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_10_12_27_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
