# 微信web开发者工具

[官方文档](https://developers.weixin.qq.com/miniprogram/dev/framework/structure.html)

[老姚文档](https://github.com/Wscats/Good-Text-Share/issues/58)

[微信小程序示例源码](https://github.com/wechat-miniprogram/miniprogram-demo)

[weui-小程序版](https://github.com/Tencent/weui-wxss/)
## 注意

- ### 尺寸单位
rpx（responsive pixel）: 可以根据屏幕宽度进行自适应。规定屏幕宽为750rpx。如在 iPhone6 上，屏幕宽度为375px，共有750个物理像素，则750rpx = 375px = 750物理像素，1rpx = 0.5px = 1物理像素。



|设备|rpx换算px (屏幕宽度/750)|px换算rpx (750/屏幕宽度)|
|-|-|-|
|iPhone5| 	1rpx = 0.42px| 	1px = 2.34rpx|
|iPhone6	|1rpx = 0.5px	|1px = 2rpx|
|iPhone6 Plus|	1rpx = 0.552px	|1px = 1.81rpx|

建议： 开发微信小程序时设计师可以用 iPhone6 作为视觉稿的标准。

注意： 在较小的屏幕上不可避免的会有一些毛刺，请在开发时尽量避免这种情况。


- ### 页面的生命周期

### onLoad(Object query)
页面加载时触发。一个页面只会调用一次，可以在 onLoad 的参数中获取打开当前页面路径中的参数。
### onShow()
页面显示/切入前台时触发。
### onReady()
页面初次渲染完成时触发。一个页面只会调用一次，代表页面已经准备妥当，可以和视图层进行交互。
### onHide()
页面隐藏/切入后台时触发。 如 navigateTo 或底部 tab 切换到其他页面，小程序切入后台等。
### onUnload()
页面卸载时触发。如redirectTo或navigateBack到其他页面时。
