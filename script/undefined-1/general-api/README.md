---
description: 전역에서 호출하기 위한 API를 소개합니다.
---

# General API

### Overview

|          API Format         | Return Value | 기능                                                  |
| :-------------------------: | :----------: | --------------------------------------------------- |
|      getObject(string)      |    object    | title값을 통해 특정 오브젝트를 선택하고 반환                         |
|   getObjectsByName(string)  |     array    | name값을 통해 같은 이름을 가진 오브젝트 배열을 반환                     |
|  onSecond(number, callback) |       -      | 지정한 시간마다 콜백 함수를 실행                                  |
|         wait(number)        |    promise   | setTimeout의 구현, 지정된 시간만큼 코드 실행을 유예                  |
| onKeyDown(string, callback) |       -      | 특정 키를 누르는 이벤트에 콜백 함수를 실행                            |
|  onKeyUp(string, callback)  |       -      | 특정 키를 떼는 이벤트에 콜백 함수를 실행                             |
|    onClickEmpty(callback)   |       -      | 플레이 모드에서 isAlive상태가 아닌 요소(지면, 허공 등)를 클릭 시 콜백 함수를 실행 |
|     changeScene(string)     |       -      | 실행 시 특정 pId값을 가지는 play mode scene으로 리다이렉트           |
|        stopAllSound()       |       -      | scene에 존재하는 모든 오디오 오브젝트를 정지                         |
|      getMousePosition()     |    object    | 호출한 시점의 마우스 포인터 좌표를 반환                              |
|  enableKeyControl(boolean)  |       -      | 키입력 이벤트를 제거/복구                                      |
|         hideAllGui()        |       -      | 모든 GUI요소를 한 번에 숨기는 기능                               |
|       getPlayerCount()      |    number    | 멀티플레이 시 현재 세션에 존재하는 유저의 수를 반환                       |
