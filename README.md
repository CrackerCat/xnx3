# xnx3-2.0.jar

快速开发工具类，用最简洁的命令实现想要的功能。

<br/>
[纯Java，跨平台，模拟按键、鼠标点击、找图、找色，实现简单按键精灵的功能 DEMO演示](http://pan.baidu.com/s/1bpHR6Y7)
<br/>辅助开发配套工具：ScreenCapture.jar<br/>
[![ScreenCapture]](http://www.xnx3.com/software/xnx3/ScreenCapture/index.html)  
[ScreenCapture]:http://www.xnx3.com/software/xnx3/ScreenCapture/sc.png "ScreenCapture.jar"  
<br/>
将指定文字发音读出：<br/>
```Java
new TTSUtil().speak("这是要读出的文字内容");
```

发送一条短信<br/>
```Java
    SendPhoneMsgUtil.send("13011658091", "这是短信内容");
```
  
发送给123456@qq.com一封邮件<br/>
```Java
    MailUtil.sendMail("123456@qq.com", "这是邮件标题", "这是内容");
```
<br/>  

微信通过openid获取用户昵称<br/>
```Java
    WeiXinUtil.getUserInfo("openid").getNickname()
```
<br/>  

当前屏幕上搜索某个图像是否存在，并拿到搜索到的图片坐标<br/>
```Java
    Robot robot = new Robot();
    robot.setSourcePath(ImageDemo.class);
    List<CoordBean> list1 = robot.imageSearch("search.png", Robot.SIM_ACCURATE);
    System.out.println("搜索到了"+list.size()+"个图片");
```
<br/>  

<h2>网游外挂制作(外挂、鼠标、键盘模拟、找图找色、Java版的按键精灵)</h2><br/>
简单操作示例：<br/>
```Java
    //所有辅助的，模拟进行某种操作(键盘、鼠标、..)要先创建此类,在new Com()时，会自动检测运行环境是否符合、部署、注册Dll
		Com com=new Com();
		//返回创建Com()的结果，如果自检过程中发现异常，创建Com失败，则调用此会返回false
		if(com.isCreateSuccess()){
			/*
			 * 这里是执行的主体了~~~~~写你想要做的事吧
			 */
			SystemUtil systemUtil=new SystemUtil(com.getActiveXComponent());
			systemUtil.beep(2000, 1000);	//蜂鸣器发音
			System.out.println("系统开机到现在运行的时间是："+systemUtil.getSystemRunTime()/1000+"秒");
		}else{
			System.out.println("创建Com对象失败");
		}
		//用完后一定要记得释放，释放内存
		com.unbind();
```
	<br/>
  简单使用请参考：<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;<a href="http://www.xnx3.com/doc/j2se_util/20150209/127.html">http://www.xnx3.com/doc/j2se_util/20150209/127.html</a><br/>

  高级使用之前台模拟操作：<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;<a href="http://www.xnx3.com/doc/j2se_util/20150209/128.html">http://www.xnx3.com/doc/j2se_util/20150210/128.html</a><br/>
  高级使用之新寻仙辅助编写：<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;<a href="http://www.xnx3.com/doc/j2se_util/20150209/129.html">http://www.xnx3.com/doc/j2se_util/20150211/129.html</a><br/>
<br/>
<h1>介绍及说明</h1><br/>
xnx3-2.0.jar <br/>
ScreenCapture.jar：纯Java编写的图片处理小工具，配合 com.xnx3.robot.Robot 进行屏幕找图的纯Java按键精灵事件操作。 <br/>
xnx3Config.xml : 若使用短信、邮件、分布式存储等功能，需在src目录下放入此配置文件。<br/>
lib/  : 支持的jar包<br/>
doc/  : xnx3-2.0.jar的doc文档<br/>
src/  : xnx3-2.0.jar的源文件<br/>
demo/ : 一些简单的demo示例<br/>
<br/>
<br/>
作者：管雷鸣<br/>
交流QQ群：418768360  <br/>
业务联系QQ：921153866<br/>
业务联系E-mail：mail@xnx3.com<br/>
