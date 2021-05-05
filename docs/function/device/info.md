
<h1 style="font-weight: bold"> 1. 디바이스 정보 조회</h1>

###  선수 작업 

자바스크립트 함수 `receiveDeviceInfo` 를 앱에서 호출합니다. 미리 웹에 선언해주세요.
```
<script>
  function receiveDeviceInfo(os, platformId, uuid) {
    alert(os);
    alert(platformId);
    alert(uuid);
  } 
</script>
```

###  요청
###### Android
```
<script>
  android.requestDeviceInfo()
</script>
```

###### iOS
```
<script>
  window.webkit.messageHandlers.requestDeviceInfo.postMessage('');
</script>
```

###  응답
```
// receiveDeviceInfo 호출됨
receiveDeviceInfo(os, platformId, uuid)
```
|키|타입| 예시| 설명 |
|---|---|---|---|
| os  | 'android' or 'ios' |  android  |  기기 OS 정보  |
| platformId  |  string  |  platform-223o23o2  | 비대칭 암호화된 앱 고유 아이디  |
| uuid  | string   |  229392912d01230d  | 비대칭 암호화된 기기 고유 아이디  |

암호화에 대한 정보는 이 [링크](/function/crypto.md)를 클릭해주세요
