# 8. 打包发布

## 发布到Web

- 顶部菜单选择项目->构建发布，选择发布平台为Web Mobile，点击构建按钮
![8-1](/8-1.png)

## 分辨率适配

- 点击运行按钮在浏览器中可以预览发布的Web平台的游戏，这里有个问题就是PC上分辨率过高，导致浏览器中查看时屏幕左右是黑块，这里我们再修改一下Canvas下的bg、ground节点，分别向左和向右增加一个子节点，以覆盖满大分辨率屏幕，具体操作方法只需要复制子节点并修改Postion数值X即可，sky同理修改一下Position和Size
![8-2](/8-2.png)
- 通过选择不同分辨率的设备浏览时，发现左上角的得分数字scoreIcon和score显示位置不固定，有时在屏幕中间有时会被遮挡住，这里我们再修改一下scoreIcon的布局，选中scoreIcon，属性检查器面板里添加Widget组件，Top=70px，Left=70px，这样就可以使他固定在屏幕左上角
![8-3](/8-3.png)
- 重新打包发布到Web Mobile平台，点击构建按钮

## 修改启动画面

- 打包后在build->web-mobile目录下有一个splash.png，是游戏的启动画面背景图，我们用自己修改的png图片替换掉它即可
- 我们将build->web-mobile目录打包压缩后部署到Nginx服务器，PC或手机浏览器打开就可以体验游戏了
![8-4](/8-4.png)

## 发布到微信小游戏

- [下载微信小游戏开发工具](https://developers.weixin.qq.com/minigame/dev/devtools/download.html)
- 顶部菜单选择Cocos Creator->偏好设置->原生开发环境->WeChat程序路径配置小游戏开发工具路径
![8-5](/8-5.png)
- 顶部菜单选择项目->构建发布，选择发布平台为Wechat Game，修改你自己的appid，点击构建按钮
![8-6](/8-6.png)
- 构建完毕后，点击运行按钮启动小游戏开发工具，进行上传和发布
![8-7](/8-7.png)