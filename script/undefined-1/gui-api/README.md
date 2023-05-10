# GUI API

### Overview

|         API Format         | Return Value | 기능                              |
| :------------------------: | :----------: | ------------------------------- |
|   sprite.setText(string)   |       -      | GUI의 innertext를 지정한 문자열로 변경     |
| sprite.setTextsize(number) |       -      | GUI의 innertext의 크기를 지정한 값으로 변경  |
|        sprite.show()       |       -      | 호출한 GUI요소가 숨겨져 있다면 다시 나오게 함     |
|        sprite.hide()       |       -      | 호출한 GUI요소를 숨김                   |
|  sprite.onClick(callback)  |       -      | GUI요소를 클릭 시 지정한 콜백 함수를 실행       |
|  sprite.setPosition(x, y)  |       -      | GUI요소의 위치를 지정한 좌표로 변경           |
|    sprite.getPosition()    |    object    | GUI의 현재 위치값을 객체로 반환 {x, y}      |
|    sprite.setScale(x, y)   |       -      | GUI의 크기를 지정한 x, y값으로 변경         |
| sprite.move(dx, dy, speed) |       -      | GUI를 지정한 dx, dy 거리만큼 지정한 속도로 이동 |



GUI등 멀티 플레이 환경에서 특정 유저에게만 보여야 하는 실행의 경우 옵션으로 api의 대상을 지정할 수 있습니다. 넣어주는 옵션의 형식은 아래와 같습니다.

```javascript
// 옵션의 형식
{target: [플레이어 배열]}

// somePlayer에게만 someGUI가 사라지도록 실행
someGUI.hide({target: [somePlayer]})

// somePlayer에게만 someGUI에 텍스트가 설정되도록 실행
someGUI.setText("your text", {target: [somePlayer]})

// 배열에 여러 플레이어를 포함할 수 있습니다.
someGUI.setText("your text", {target: [somePlayer1, somePlayer2 ...]})

// audio, gui setting
// Wrong way (X) - execute in global scope
someGUI1.hide({target: [player]})
someGUI2.hide({target: [player]})
someAudio.stopAudio({target: [player]})

// proper way (O) - execute in onjoinplayer
function OnJoinPlayer(player) {
	someGUI1.hide({target: [player]})
	someGUI2.hide({target: [player]})
	someAudio.stopAudio({target: [player]})
}
```
