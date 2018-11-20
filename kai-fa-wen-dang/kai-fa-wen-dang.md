---
description: Jike Open platfrom JavaScript SDK
---

# 开发文档

### Installation

```bash
npm install jike-open-js-sdk --save
```

### Configuration

```bash
import { JikeOpenJsSDK } from 'jike-open-js-sdk'
// FIST OF ALL: apply for your application at jike open platform.
// replace <openAppId> with your openAppId.
const sdk = new JikeOpenJsSDK(<openAppId>)
// or
const sdk = new JikeOpenJsSDK({
  openAppId: <openAppId>
})
```

### API

> sdkInstance.getUserInfo\(\)

* available version 4.15.0

```text
sdkInstance.getUserInfo(): Promise<UserInfo>
```

> sdkInstance.getMessages\(\)

* available version 4.15.0

```text
sdkInstance.getMessages(): Promise<{
  message: Array<Message>
  count: number
}>
```

### Interface

> UserInfo

```bash
interface UserInfo {
  user: {
    id: string,
    isLoginUser: boolean,
    screenName: string,
    profileImage: {
      format: string,
      picUrl: string,
      middlePicUrl: string,
      thumbnailUrl: string,
    }
  }
}

type Message = Record<string, any>
```

