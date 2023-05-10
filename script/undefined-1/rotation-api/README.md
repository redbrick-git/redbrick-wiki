# Rotation API

### Overview

|        API Format       | Return Value | 기능                                |
| :---------------------: | :----------: | --------------------------------- |
|    object.rotateX(dx)   |       -      | 오브젝트를 x축으로 지정한 만큼 바로 회전           |
|    object.rotateY(dy)   |       -      | 오브젝트를 y축으로 지정한 만큼 바로 회전           |
|    object.rotateZ(dz)   |       -      | 오브젝트를 z축으로 지정한 만큼 바로 회전           |
| object.turnX(dx, speed) |       -      | 오브젝트를 x축으로 지정한 속도로 지정한 각도만큼 회전    |
| object.turnY(dy, speed) |       -      | 오브젝트를 y축으로 지정한 속도로 지정한 각도만큼 회전    |
| object.turnZ(dz, speed) |       -      | 오브젝트를 z축으로 지정한 속도로 지정한 각도만큼 회전    |
|   object.getRotation()  |    object    | 오브젝트의 rotation값을 객체로 반환 {x, y, z} |
