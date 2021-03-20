# 小米运动自动刷步数

> 小米运动自动刷步数

## Github Actions 部署指南

### 一、Fork 此仓库

### 二、设置账号密码

添加名为  **PMODE**、**PKEY**、**USER**、**PWD**、**STEP** 的变量，值分别为 **PMODE推送模式（ 'wx' server酱推送 'nwx' 新server酱推送 'tg' tg推送 ）**、 **推送key（0关闭）**、 **账号（仅支持手机号）**、**密码**、**步数（0则为1w-2w之间随机 或自定义随机范围[18000-25000]）**

> Settings-->Secrets-->New secret

### 三、多账户(用不上请忽略)

多账户请用 **#** 分割 然后保存到变量 **USER** 和 **PWD**

#### 例如

**13800138000#13800138001** 变量 **USER**

**abc123qwe#abcqwe2** 变量 **PWD**

### 四、自定义启动时间

编辑 **.github/workflows/run.yml**

找到 cron: 0 10 * * *

修改其中的10为你要的时间

需要运行的时间-8就是UTC时间

### 五、消息推送

如果使用server酱推送 **PKEY** 填写server酱的推送key

如果使用tg推送 **PKEY** 填写 **token-userid**

## 注意事项

1. 每天运行一次，在下午 6 点

2. 多账户的数量和密码请一定要对上 不然无法使用!!!

3. 启动时间得是UTC时间!

4. server酱注册地址 [点我](https://sct.ftqq.com/)

5. 如果支付宝没有更新步数,到小米运动->设置->账号->注销账号->清空数据,然后重新登录,重新绑定第三方

6. 小米运动不会更新步数，只有关联的会同步！！！！！

7. 请各位在使用时Fork[主分支](https://github.com/Squaregentleman/mimotion/)，防止出现不必要的bug.

8. TG推送教程 [点我](./TG_PUSH.md)

## 历史Star数

[![Stargazers over time](https://starchart.cc/Squaregentleman/mimotion.svg)](https://starchart.cc/Squaregentleman/mimotion)