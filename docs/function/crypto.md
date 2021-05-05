# 1. 대칭키 암호화
대칭키 암호화는 `AES/CBC/PKCS5Padding` 알고리즘을 사용하고 있습니다. 

## 선행
- key 정보를 미리 요청해주셔야합니다.

## PHP
### 암호화
```
function AESEncrypt($str, $key){
    return base64_encode(openssl_encrypt($str, "AES-256-CBC", $key, true, str_repeat(chr(0), 16)));
}
```

### 복호화
```
function AESDecrypt($str, $key){
    return openssl_decrypt(base64_decode($str), "AES-256-CBC", $key, true, str_repeat(chr(0), 16));
}
```
