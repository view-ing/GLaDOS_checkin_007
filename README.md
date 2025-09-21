# GLaDOS 自动签到，实现无限白嫖

原仓库地址：https://github.com/lukesyy/glados_automation

复制了一个仓库，进行了些修改，防止原仓库被封

环境变量：`GLADOS_COOKIE`（必要） 和 `PUSHPLUS_TOKEN`（非必要）

`GLADOS_COOKIE`多个账号需使用 '&' 隔开，示例：cookie&cookie


# Github Actions 使用方法

1. 点击右上角 **fork** 按钮
2. 登录GLaDOS后获取cookies。（简单获取方法：浏览器快捷键F12，打开调试窗口，点击“network”获取）
3. 在自己仓库中打开此项目
4. 将 `runGladosAction.yml` 放入 `.github/workflows` 文件夹下
5. 在自己的仓库`Settings`里创建2个`Secrets`(配置环境变量)
    - GLADOS_COOKIE**必填**）
    - PUSHPLUS_TOKEN （填写pushplus的token，不开启则不用填）
6. 点亮右上角的星星 **star** 激活 actions
7. 然后点击 Actions 标签查看运行的详细状况

8. 以上设置完毕后，每天零点会自动触发，并会执行自动checkin，如果开启pushplus，会自动发通知到微信上。

![image](https://user-images.githubusercontent.com/70319988/231369203-c812910a-963d-45b8-98a5-95b2623c25d7.png)
![image](https://user-images.githubusercontent.com/70319988/199923789-639e8295-b03e-4abd-858e-ff427015512a.png)
![image](https://user-images.githubusercontent.com/70319988/199923884-d81dd457-ecc5-4de9-b480-191d25217c47.png)

 # 青龙面板

直接把 glados_Qinglong.py 文件放到青龙里，环境变量同上


# 脚本功能：

1、通过Github Action自动定时运行[glados.py](https://github.com/view-ing/GLaDOS_checkin_007/blob/main/glados.py)脚本。

2、通过cookies自动登录（[https://glados.rocks/console/checkin](https://glados.rocks/console/checkin))，脚本会自动进行checkin，可实现多个账号签到。

3、然后通过“pushplus”（[https://www.pushplus.plus/](https://www.pushplus.plus/))，自动发通知到微信上。

