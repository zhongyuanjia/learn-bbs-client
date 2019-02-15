-----------
# 管理员专属
#### 功能

> 获取用户列表

#### URL

> GET /api/v1/users?offset=0&limit=5

#### 请求参数

|参数|必选|类型|默认值|说明|
|:----- |:-------|:------|:-----|----- |
|offset|false|int|0| 从第几个开始|
|limit|false|int|5| 获取几个|

#### 返回字段
|返回字段|字段类型|说明 |
|:----- |:------|:----------------------------- |
|data | Array\<user> | 用户列表 |
|total | int | 用户数量 |

#### 响应：
##### 成功：200
响应格式：JSON
```
{
  "data": [
    {
      "id": "user-id"
      // 其他数据同getUser的数据
    }
  ],
  "total": 400
}
```
##### 未登录: 401
##### 权限不足: 403