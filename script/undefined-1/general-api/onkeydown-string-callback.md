# onKeyDown(string, callback)

### 정의

> ### 특정 키를 누르는 이벤트에 콜백 함수를 실행합니다.
>
> * **string**\
>   Key\[key] 형태로 키를 입력합니다.\
>   아바타 기본 조작키 (w, a, s, d, space)는 사용하지 않습니다.
> * **callback(args)**\
>   키를 누르면 실행될 코드를 입력합니다.



### 예시

<pre class="language-javascript"><code class="lang-javascript">const sphere = getObject("SPHERE(cc6)")
onKeyDown("KeyZ", function() {
    sphere.goX(-1)
})

onKeyDown("KeyX", function() {
    sphere.goX(1)
})

<strong>// multiplay example
</strong>onKeyDown("KeyM", function(player) {
    // player는 event를 발생시킨 주체이며 doSomething은 예시 코드입니다.
    player.doSometing(
})
</code></pre>

<figure><img src="../../../.gitbook/assets/화면_기록_2022-12-14_오후_9_47_18_AdobeExpress (1).gif" alt=""><figcaption><p>실행 결과</p></figcaption></figure>
