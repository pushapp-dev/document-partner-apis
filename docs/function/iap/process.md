
# 1. 결제 요청

###  요청
###### Android
```
<script>
  const payload = { orderId: '1', code: 'apple_200' };    
  const jsonString = JSON.stringify(a);
  android.purchase(jsonString);
</script>
```

###### iOS
```
<script>
  const payload = { orderId: '1', code: 'apple_200' };    
  const jsonString = JSON.stringify(a);
  window.webkit.messageHandlers.purchase.postMessage(jsonString);
</script>
```
