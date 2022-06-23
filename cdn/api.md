# API接口

## 注册

### 获取验证码

目前有4种短信验证码，对应的type是：
- 注册短信验证码： register
- 修改密码短信验证码: changePassword
- 修改手机短信验证码: changePhoneNumber
- 验证手机号短信验证码: verifyPhoneNumber
#### Request
- Method: **GET**
- URL:  ```/v1.0/open/smscode?type={type}&phone={phone}```
    - register for new user:  ```/v1.0/open/smscode?type=register&phone=13811119999```
    - forgot password: ```/v1.0/open/smscode?type=changePassword&phone=13822224444```
- Headers：
- Body:
```
```

#### Response
- Body
```
{
  "code": 200,
  "data": "730781",
  "message": "OK"
}
```

注意：为了防止短信验证码被滥用，短信如果发送后，需要隔60s才能重新发送。
