---
layout: cover
---
# react-packup

---

# 数据库

* pkg

  | column | id     | pkgId  | userId | content | state  |
  | ------ | ------ | ------ | ------ | ------- | ------ |
  | value  | number | string | string | string  | string |

---

# 数据库

* *pkgState*

  | column | id     | pkgId  | userid | time | state | reason |
  | ------ | ------ | ------ | ------ | ---- | ----- | ------ |
  | value  | number | string | string | Date | enum  | string |

---

# 数据库

* user

  | column | id   | userid | username | password | college | name   | tel    | address | isActive |
  | ------ | ---- | ------ | -------- | -------- | ------- | ------ | ------ | ------- | -------- |
  | value  |      | string | string   | string   | string  | string | string | string  | boolean  |

---

# 前端页面

* 登录
* home：当前用户所有包裹
* info：个人信息
* 扫码===page ？ page ： Modal
* 调用相机界面
  * 扫码完成的权限管理
    * （学生）收发：扫码获得 pkgId => 获得不同状态（无包裹/进行中/到站） => 输入 content 来 init/提示正在路上/确认签收
    * （staff）登记：只负责扫码、点确认，每个 staff 对应一个 state 和 reason（根据 address 和 tel 自动合成），可以在 info 修改
    * （mobile admin）强制 init，强制 finish
* admin 管理页面（抄一个）
