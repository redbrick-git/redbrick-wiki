# object.playAnimation(string)

### 정의

> ### 실행 시 지정한 애니메이션 실행합니다.
>
> * 레드브릭 기본 아바타에 한하여 사용 가능합니다.
> * **string**\
>   victory, die



### 예시

```javascript
const tree = getObject("nature_minitree1_006(c3e)")

function OnJoinPlayer(player) {
	tree.onCollide(player, function() {
	    tree.kill()
	    player.playAnimation("victory")
	})
}
```
