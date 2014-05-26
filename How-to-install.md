1、	通过链接https://github.com/Countly/countly-sdk-ios 下载Countly IOS SDK.  
2、	在Xcode中将以下文件添加到项目中：Countly.h Countly.m Countly_OpenUDID.h Countly_OpenUDID.m CountlyDB.h CountlyDB.m 和 Countly.xcdatamodeld  
3、	对于OS X系统，请直接跳至第11步。对于IOS系统，继续第4步。  
4、	在项目导航中选中要集成的项目。  
5、	选择“编译阶段(Build Phases)”选项卡。  
6、	找到“Link Binaries With Libraries”展开标识。  
7、	点击“+”。  
8、	选择“CoreTelephony.framework”，选择“Optional”。  
9、选择“CoreData.framework”。  
10、把添加的framework拖拽到Frameworks group中。  
11、在应用的delegate中引入Countly.h，在application:didFinishLaunchingWithOptions:的方法开始处添加以下代码：  
[[Countly sharedInstance] start:@"YOUR_APP_KEY" withHost:@"https://api.qiku.mobi"]  
其中YOUR_APP_KEY请替换为奇酷分配的KEY。
