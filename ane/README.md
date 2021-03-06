#ANE详细使用说明

- [奇虎360](#奇虎360)
- [海马](#海马)
- [爱思助手](#爱思助手)
- [同步推](#同步推)
- [iTools](#itools)
- [快用](#快用)
- [果盘叉叉助手](#叉叉助手)
- [XY助手](#xy助手)
- [PP助手](#pp助手)

## 奇虎360

SDK及文档地址[点此](http://dev.360.cn/wiki/index/id/73)  

集成SDK版本v1.1.8(402).  

使用时注意替换Demo配置文件`ANEDemo.xml`中的参数为正式参数:  
`QHOPENSDK_APPID`、`QHOPENSDK_APPKEY`的值为在360申请的appid和appkey  
`QHOPENSDK_PRIVATEKEY`的值为`md5(app_secret +”#”+ app_key)`     
`QHOPENSDK_WEIXIN_APPID` 用于微信分享，如使用需要到微信开放平台申请ID  

登录结果中token即为access_token，需要通过服务端换取用户ID。查看[获取用户信息](http://dev.360.cn/wiki/index/id/67)  
支付时需要加上以下属性:  
- `pay.qihooUid` 奇虎用户ID
- `pay.uname`  用户名
- `pay.uid`    用户id
- `pay.notifyUrl` 通知地址
查看[支付结果通知服务端接口](http://dev.360.cn/wiki/index/id/68)

支持的其他操作
- `uploadScore`      上传积分
- `destroy`          销毁
- `antiAddiction`	   防沉迷
- `realNameRegister` 实名注册


## <span id="qihoo360">海马</span>

查看[联运平台](http://pay.haima.me)   
需要通过海马审核才能使用SDK，否则会显示应用被禁用

Android海马SDK版本为v1.1.4  
iOS海马SDK版本v1.3.6

> Demo测试参数
	
	//ios
	init.appId = "17dcfe3ac35e8b65a7bd13785ca2d800";

	//android
	init.appId = "e5dc65b49905df4b3e618d7eac2117ea";

## 爱思助手
iOS SDK版本v2.1.0  

修改配置文件, As2中的2修改为在爱思后台申请的appId.

	<key>CFBundleURLSchemes</key>
	<array>
		<string>As2</string>
	</array>

> Demo测试参数

	init.appId = 2;
	init.appKey = "118255f8ffec4352a919c52d01a2d674";

## 同步推
iOS SDK版本v4.1.2

> Demo测试参数
	
	init.appId = 100000;

## iTools
iOS SDK版本v2.5.0

> Demo测试参数

	init.appId = 1;
	init.appKey = "58C6A68DDDEE471AA43266E427F38D92";

## 快用
iOS SDK版本v2.2.3  
Android SDK版本v2.0.3

**由于快用iOS的库使用了Embedded Frameworks，而air打包时不会对其重新签名。导致最终的包与库签名不同。  
使用[iReSign](https://github.com/maciekish/iReSign)将生成的包重新签名即可正常**

> Demo测试参数
     
    //ios 包名必须为 com.ky.xSDK.demo
	init.appKey = "edfd2ae4098863890c1a01b5d7b76d55";
	pay.payID = "100087";

	//android 包名 com.youran.KyUserDemo
	init.appKey = "f8ad685fcaf0e92b2fe9c5c7c822610e";
	pay.payID = "100246";

## 叉叉助手
iOS SDK版本v2.0.0
包名(bundle/package id)需要以.guopan结尾

打包有问题，暂时还不能用。。。

> Demo测试参数
	
	init.appId = "101101";
	init.appKey = "GuopanSDK8^(Llad";

## XY助手
iOS SDK版本v2.1.1


> Demo
	
	//ios包名com.xy.sdk
	init.appId = "100009";
	init.appKey = "cZZqE43VLVjUC7YxpnBpnwrZ1NMyfuW6"


## PP助手
iOS SDK版本vS155D1571
修改配置文件中 teiron76 中的76为自己的appid

> Demo
	
	init.appId = "5747";
	init.appKey = "c5ebb80ee40060baaf381f2d7da1ce23"


## 其他
TODO
