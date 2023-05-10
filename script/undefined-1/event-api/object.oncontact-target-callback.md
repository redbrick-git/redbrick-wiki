# object.onContact(target, callback)

### 정의

> ### 오브젝트에 타겟이 충돌한 후 접촉한 상태일 경우 콜백 함수를 반복적으로 실행합니다.
>
> * **target**\
>   접촉했는지 판단할 타겟을 입력합니다.\
>   아바타의 경우 player를 입력합니다.
> * **callback(args)**\
>   반복적으로 실행될 코드를 입력합니다.



### 예시

```javascript
const tile = getObject("decoration_concretetile_001(dcc)")

function OnJoinPlayer(player) {
	tile.onContact(player, function() {
	    tile.moveX(1, 10)
	})
}

// multiplay project
function OnJoinPlayer(player) {
	tile.onContact(player, function(target) {
	    tile.kill()
	    wait(1)
	    tile.revive()
	    // target.doSomething()
	})
}
```

<figure><img src="../../../.gitbook/assets/onContact.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
