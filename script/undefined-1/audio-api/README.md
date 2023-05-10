# Audio API

### Overview

|           API Format           | Return Value | 기능                                     |
| :----------------------------: | :----------: | -------------------------------------- |
|       object.playAudio()       |       -      | 오디오 오브젝트의 음원을 시작(pause되었다면 멈춘 부분부터 시작) |
|       object.pauseAudio()      |       -      | 오디오 오브젝트의 음원을 일시정지                     |
|       object.stopAudio()       |       -      | 오디오 오브젝트의 음원을 정지(처음 부분으로 되돌림)          |
|    object.setVolume(number)    |       -      | 오디오 오브젝트의 음량을 설정                       |
| object.setPlaybackRate(number) |       -      | 오디오 오브젝트의 음원 재생속도를 설정                  |
|       object.getVolume()       |    number    | 오디오 오브젝트의 현재 음량을 반환                    |
