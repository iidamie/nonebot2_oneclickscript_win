# NoneBot2 Windows 一键部署脚本

## 要求

- Python `3.10.x`（安装时记得勾选 `Add Python 3.10 to PATH` !!!）
- [Python推荐下载链接](https://registry.npmmirror.com/binary.html?path=python/3.10.9/)在这里根据自己的系统下载对应版本

## 如何使用

1. 运行 `#配置环境.bat` ，按照指引即可
2. 然后打开 `go-cqhttp` 文件夹，打开 `config.yml` 按照提示修改账号相关内容
3. 修改好后32位系统运行 `go-cqhttp_x32.bat` ,64位系统运行 `go-cqhttp_x64.bat` ，按照提示登录账号
- 如果无法登录账号，[点击我](https://docs.qq.com/doc/DQ3lmbkVUTkhiUWxM?&u=dc6ddf501e234007b2b1f2efea165532)查看解决办法
4. 完成以上步骤之后，运行 `#启动.bat` ，你的 Bot 就成功运行了！
- 试试向 Bot 发送指令 `ping` ，如果 Bot 回复了就代表配置没有问题啦~
## 进阶使用

### 切换连接方式 / 使用其他适配器 / 使用其他驱动器

我已经在 `pyproject.toml`、`.env`、`bot.py` 文件里写好了注释，按照对应文档稍微编辑一下即可

### 安装 / 卸载插件

#### 安装商店插件

1. 运行 `#进入虚拟环境.bat`
2. 粘贴从插件市场里复制下来的 `nb plugin install 插件名` 格式的指令，按下回车
3. 根据插件文档在 `.env` 文件里纂写配置项
4. 如果 NoneBot 正在运行，关掉 NoneBot 后重新开启即可

#### 卸载商店插件

1. 运行 `#进入虚拟环境.bat`
2. 输入 `nb plugin uninstall 插件名`，插件名支持模糊检索
3. 如果卸载报错 `拒绝访问` ，请关掉 NoneBot 后重试
4. 如果 NoneBot 正在运行，关掉 NoneBot 后重新开启即可

#### 安装第三方插件

1. 在 `src/plugins` 文件夹放入第三方插件
2. 运行 `#进入虚拟环境.bat`
3. 安装插件依赖
4. 如果 NoneBot 正在运行，关掉 NoneBot 后重新开启即可

#### 卸载第三方插件

1. 从 `src/plugins` 文件夹删除对应插件
2. 如果 NoneBot 正在运行，关掉 NoneBot 后重新开启即可
