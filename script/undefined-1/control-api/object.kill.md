# object.kill()

### 정의

> ### 실행 시 오브젝트를 화면에서 보이지 않도록 처리합니다.
>
> * revive()를 활용하여 사라진 오브젝트를 되살릴 수 있습니다.



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

