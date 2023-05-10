---
description: 텍스트코딩에 대해 안내합니다.
---

# 텍스트코딩

### Overview

텍스트코딩 프로젝트의 스크립트 창을 열면 기본 제공되는 함수 Setup()과 OnJoinPlayer()가 존재합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2022-12-13 오후 1.19.37.png" alt=""><figcaption><p>Script - textcoding</p></figcaption></figure>



Setup() 내에는 기본적으로 한 번만 실행될 함수들이 들어가며,

OnJoinPlayer() 는 새로운 유저가 들어올 때마다 실행됩니다.

```javascript
function Setup() {
//...only calls one time
}

function OnJoinPlayer(player) {
//...calls every user join event
}
```



레드브릭 스튜디오에서 특정 오브젝트에 명령을 내리고 싶다면 **getObject("title").명령어**의 형태로 스크립트를 작성해야 합니다.&#x20;

{% hint style="info" %}
title에는 오브젝트 옵션 메뉴 > Script 박스 체크 후, Title에 나타나는 오브젝트명을 입력합니다.

![](<../../.gitbook/assets/스크린샷 2022-12-14 오후 2.54.05.png>)
{% endhint %}



오브젝트는 변수 및 상수에 담아 사용하면 편리합니다.

```javascript
// 전역에서 사용할 변수 및 상수 선언
const cube = getObject("cube")

function Setup() {
//...only calls one time
}

function OnJoinPlayer(player) {
//...calls every user join event
}
```



플레이어를 getObject하고 싶다면, 아래와 같은 형식으로 사용합니다.

{% hint style="info" %}
여러 명의 플레이어 정보를 저장하여, 멀티플레이가 가능하도록 하기 위함입니다.
{% endhint %}

```javascript
// 전역에서 사용하는 값, 서버 컨텍트스에서 사용하는 값이므로 모든 유저가 공유
const cube = getObject("cube")

// 플레이어를 담아 둘 저장 공간 예시
const playersArray = []
const playersObject = {}

function Setup() {
//...only calls one time
}

function OnJoinPlayer(player) {
  //접속한 플레이어를 playersArray에 저장
  playersArray.push(player)
  playersObject[player.title] = player
}
```

