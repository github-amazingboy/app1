# NGX-SMSCountDown

在注册或登录页面常有 发送短信验证码或邮箱验证码等数秒操作

[![NPM version](https://img.shields.io/npm/v/smscount-down.svg)](https://www.npmjs.com/package/ngx-smscount-down)

## Usage

### 1. Install

```
npm install ngx-smscountdown --save
```

import `SMSCountDownModule`。

```typescript
import { SMSCountDownModule } from 'smscount-down;

@NgModule({
  imports: [ BrowserModule, SMSCountDownModule ],
  declarations: [AppComponent],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

### 2、Template

```html
<button SMSCountDown Text="发送短信验证码" CountText="{leftSec}秒后可重发" [SendFun]="sendSMS">发送短信验证码</button>

<button SMSCountDown Text="发送邮箱验证码" CountText="重发剩余{leftSec}秒..." CompleteText="重新发送" [MaxCounting]="8" [SendFun]="sendSMS">发送邮箱验证码</button>
```