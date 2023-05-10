# object.revive()

### 정의

> ### 실행 시 kill된 오브젝트를 다시 나타나도록 합니다.



### 예시

```javascript
const dia = getObject("decoration_cutediamond_005(0ec)")

function OnJoinPlayer(player) {
	dia.onCollide(player, function() {
	    dia.kill()
	    wait(1)
	    dia.revive()
	})
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_9_47_26_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>

