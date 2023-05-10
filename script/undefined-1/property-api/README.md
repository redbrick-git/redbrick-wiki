---
description: 오브젝트의 속성과 관련된 API를 소개합니다.
---

# Property API

### Overview

|                 API Format                | Return Value | 기능                                                              |
| :---------------------------------------: | :----------: | --------------------------------------------------------------- |
|         object.setShadow(boolean)         |       -      | 오브젝트가 빛에 의해 그림자가 생기는지 여부를 조정                                    |
|         object.takeShadow(boolean)        |       -      | 오브젝트 표면에 그림자가 드리워지는지 여부를 조정                                     |
|         object.setMovable(boolean)        |       -      | 오브젝트의 물리엔진 적용 여부를 설정, true로 설정 시 물리엔진의 영향을 받고 false로 설정 시 받지 않음 |
| object.applyForce(number, number, number) |       -      | 바디가 있는 오브젝트에 x, y, z를 벡터로 하는 힘을 가함                              |
|  object.setTextureOffset(number, number)  |       -      | 오브젝트에 적용된 텍스쳐가 있다면 텍스쳐의 오프셋을 지정된 값으로 변경                         |
|           object.setTag(string)           |              | 오브젝트의 tag 속성을 string 값으로 설정합니다.                                 |
|             object.removeTag()            |              | 오브젝트의 tag 속성에 undefined값을 할당합니다.                                |

