# object.onCollideOnce(target, callback)

### 정의

> ### 오브젝트에 특정 타겟이 충돌했을 때 콜백 함수를 한 번만 실행합니다.
>
> * onCollide와 달리 콜백 함수는 최초 충돌시에만 호출됩니다.
> * **target**\
>   충돌했는지 판단할 타겟을 입력합니다.\
>   아바타의 경우 player를 입력합니다.
> * **callback(args)**\
>   타겟이 충돌했을 때 실행될 코드를 입력합니다.



### 예시

```javascript
const dia = getObject("decoration_cutediamond_005(0ec)")

// singleplay project
function OnJoinPlayer(player) {
	dia.onCollideOnce(player, function() {
	    dia.kill()
	    wait(1)
	    dia.revive()
	})
}

// multiplay project
function OnJoinPlayer(player) {
	dia.onCollideOnce(player, function(target) {
	    dia.kill()
	    wait(1)
	    dia.revive()
	    // target.doSomething()
	})
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_9_49_52_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
