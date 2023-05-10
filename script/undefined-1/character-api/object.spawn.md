# object.spawn()

### 정의

> ### 실행 시 시작포인트 오브젝트로 이동합니다.
>
> * 괄호 안에 오브젝트 이름을 입력하면, 해당 오브젝트로 이동합니다.
> * 입력하지 않는 경우, starting point 오브젝트로 이동합니다.



### 예시

```javascript
const tree = getObject("nature_minitree1_006(c3e)")

function OnJoinPlayer(player) {
	tree.onCollide(player, function() {
	    player.spawn()
	})
}
```

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_11_06_41_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>

<pre class="language-javascript"><code class="lang-javascript"><strong>const tree = getObject("nature_minitree1_006(c3e)")
</strong>const tile = getObject("decoration_concretetile_001(e52)")

function OnJoinPlayer(player) {
	tree.onCollide(player, function() {
	    player.spawn(tile)
	})
}
</code></pre>

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-20_오후_11_05_41_AdobeExpress.gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
