# Android

## 基础

### <span id="android_base_1">1. 四大组件是什么？</span>
“Android有四大组件:Activity、Service、Broadcast Receiver、Content Provider”
[https://blog.csdn.net/qq_41801699/article/details/79471956](https://blog.csdn.net/qq_41801699/article/details/79471956)
### <span id="android_base_2">2. Activity 的生命周期？</span>
“Activity 的生命周期: onCreate、onStart、onResume、onPause，onStop，onDestroy，onRestart”
[https://www.jianshu.com/p/fb44584daee3](https://www.jianshu.com/p/fb44584daee3)
### <span id="android_base_3">3. Activity 之间的通信方式？</span>
[https://www.jianshu.com/p/12438e23c6b8](https://www.jianshu.com/p/12438e23c6b8)
### <span id="android_base_4">4. Activity 各种情况下的生命周期？</span>
[https://www.jianshu.com/p/e46d449467d5](https://www.jianshu.com/p/e46d449467d5)
### <span id="android_base_5">5. 横竖屏切换时 Activity 的生命周期</span>
[https://www.jianshu.com/p/8c40829905ec](https://www.jianshu.com/p/8c40829905ec)
### <span id="android_base_6">6. 前台切换到后台，然后再回到前台时 Activity 的生命周期</span>
A调用onCreate()方法 ---> onStart()方法 ---> onResume()方法。当A启动B时，A调用onPause()方法，然后调用新的Activity B，此时调用onCreate()方法 ---> onStart()方法 ---> onResume()方法将新Activity激活。之后A再调用onStop()方法。当A再次回到前台时，B调用onPause()方法，A调用onRestart()方法 ---> onStart()方法 ---> onResume()方法，最后调用B的onStop()方法 ---> onDestory()方法。
### <span id="android_base_7">7. 弹出 Dialog 的时候按 Home 键时 Activity 的生命周期</span>
当我们的Activity上弹出Dialog对话框时，程序的生命周期依然是onCreate() ---> onStart() ---> onResume()，在弹出Dialog的时候并没有onPause()和onStop()方法。而在此时我们按下Home键，才会继续执行onPause()和onStop()方法。这说明对话框并没有使Activity进入后台，而是在点击了Home键后Activity才进入后台工作。

原因就是，其实Dialog是Activity的一个组件，此时Activity并不是不可见，而是被Dialog组件覆盖了其他的组件，此时我们无法对其他组件进行操作而已。
### <span id="android_base_8">8. 两个 Activity 之间跳转时的生命周期</span>
[https://www.cnblogs.com/yjing/p/5263109.html](https://www.cnblogs.com/yjing/p/5263109.html)
### <span id="android_base_9">9. 下拉状态栏时 Activity 的生命周期</span>
下拉通知栏对Activity的生命周期没有影响。
### <span id="android_base_10">10. Activity 与 Fragment 之间生命周期比较？</span>
[https://www.jianshu.com/p/5b132124cafc](https://www.jianshu.com/p/5b132124cafc)
### <span id="android_base_11">11. Activity 的四种 LaunchMode（启动模式）的区别？</span>
1.standard
standard模式是默认的启动模式，不用为<activity>配置android:launchMode属性即可，当然也可以指定值为standard。

2.singleTop
在上面的基础上为<activity>指定属性android:launchMode="singleTop"，系统就会按照singleTop启动模式处理跳转行为。singleTop启动模式，如果发现有对应的Activity实例正位于栈顶，则重复利用，不再生成新的实例。

3.singleTask
在上面的基础上修改FActivity的属性android:launchMode="singleTask"。singleTask模式，如果发现有对应的Activity实例，则使此Activity实例之上的其他Activity实例统统出栈，使此Activity实例成为栈顶对象，显示到幕前。

4.singleInstance
这种启动模式比较特殊，因为它会启用一个新的栈结构，将Acitvity放置于这个新的栈结构中，并保证不再有其他Activity实例进入。
### <span id="android_base_12">12. Activity 状态保存与恢复？</span>
[https://www.jianshu.com/p/715333d87738](https://www.jianshu.com/p/715333d87738)  
[https://www.jianshu.com/p/6968cca44763](https://www.jianshu.com/p/6968cca44763)
### <span id="android_base_13">13. Fragment 各种情况下的生命周期？</span>
[https://blog.csdn.net/jokeeeeee/article/details/46004931](https://blog.csdn.net/jokeeeeee/article/details/46004931)  
[https://blog.csdn.net/ya1139569539/article/details/78192112](https://blog.csdn.net/ya1139569539/article/details/78192112)  
[https://blog.csdn.net/lmj623565791/article/details/37970961](https://blog.csdn.net/lmj623565791/article/details/37970961)
### <span id="android_base_14">14. Activity 和 Fragment 之间怎么通信， Fragment 和 Fragment 怎么通信？</span>

	Activity 传值给 Fragment：通过 Bundle 对象来传递，Activity 中构造 bundle 数据包，调用 Fragment 对象的 `setArguments(Bundle b)` 方法，Fragment 中使用 `getArguments()` 方法获取 Activity 传递过来的数据包取值。
	
	Fragment 传值给 Activity：在 Fragment 中定义一个内部回调接口，Activity 实现该回调接口， Fragment 中获取 Activity 的引用，调用 Activity 实现的业务方法。接口回调机制式 Java 不同对象之间数据交互的通用方法。
	
	Fragment 传值给 Fragment：一个 Fragment 通过 Activity 获取到另外一个 Fragment 直接调用方法传值。

### <span id="android_base_15">15. Service 的生命周期？</span>
[https://www.jianshu.com/p/cc25fbb5c0b3](https://www.jianshu.com/p/cc25fbb5c0b3)
### <span id="android_base_16">16. Service 的启动方式？</span>
Service 的启动方式有两种，一种是startService(),一种是bindService().这两种方式有有什么区别.

startService()，启动完之后该service就在后台运行，其生命周期跟启动它的Context没有任何关系。也不能跟Context通讯。
bindService()启动之后生命周期跟启动它的Context有关，比如Activity、fragment、service等。在Context中解绑之后，如果改Service没有任何绑定后该Service也就结束。

### <span id="android_base_17">17. Service 与 IntentService 的区别?</span>
Service简介  
- 四大组件之一，没有用户界面，运行在后台。通常用于执行一些后台任务。例如，音乐播放等；
- 继承于ContextWrapper，ContextWrapper继承于Context；
- Service不是单独的进程，也不是线程，它和线程没有任何关系。它运行在主线程中，因此不能直接执行
耗时任务。否则可能会导致ANR。如果需要执行耗时任务则需要创建独立的线程来执行；

IntentService简介：  
- IntentService 是 Service 的子类，因此具有和 Service 一样的生命周期，同时也提供了在后台
线程中处理异步任务的机制。这个后台线程就是HandlerThread(后面做详解)；
- 启动 IntentService 的方式和启动 Service 是一样的。不同的是 Service
 执行完后需要手动停止，而 IntentService 则不需要。任务执行完毕会自动停止(原理在后面做详解)；
- 可以启动 IntentService 多次，如果此时IntentService正在运行，则这个新的Intent将会进入队
列,排队等候执行。如果此时IntentService没有在运行，则会启动一个新的IntentService。这是一个
单线程操作，前面的任务处理完了，后面的任务才能被处理（原理在后面详解）；

[https://www.jianshu.com/p/ea8bc4aaf057](https://www.jianshu.com/p/ea8bc4aaf057)
### <span id="android_base_18">18. Service 和 Activity 之间的通信方式？</span>

- 通过 Binder 对象
- 通过 Broadcast（广播）的形式

### <span id="android_base_19">19. 对 ContentProvider 的理解？</span>
[https://www.jianshu.com/p/92649b08ab4e](https://www.jianshu.com/p/92649b08ab4e)
### <span id="android_base_20">20. ContentProvider、ContentResolver、ContentObserver 之间的关系？</span>
ContentProvider——内容提供者， 在android中的作用是对外共享数据，也就是说你可以通过ContentProvider把应用中的数据共享给其他应用访问，其他应用可以通过ContentProvider 对你应用中的数据进行添删改查。   
ContentResolver——内容解析者， 其作用是按照一定规则访问内容提供者的数据（其实就是调用内容提供者自定义的接口来操作它的数据）。   
ContentObserver——内容观察者，目的是观察(捕捉)特定Uri引起的数据库的变化，继而做一些相应的处理，它类似于数据库技术中的触发器(Trigger)，当ContentObserver所观察的Uri发生变化时，便会触发它。

### <span id="android_base_21">21. 对 BroadcastReceiver 的了解？</span>
[https://www.jianshu.com/p/989e7c2f9293](https://www.jianshu.com/p/989e7c2f9293)
### <span id="android_base_22">22. 广播的分类？使用方式和场景？</span>
[https://www.jianshu.com/p/02c9ddcd9a47](https://www.jianshu.com/p/02c9ddcd9a47)
### <span id="android_base_23">23. 动态广播和静态广播有什么区别？</span>

- 动态的比静态的安全
- 静态在 App 启动的时候就初始化了，动态使用代码初始化
- 静态需要配置，动态不需要
- 生存期，静态广播的生存期可以比动态广播的长很多
- 优先级动态广播的优先级比静态广播高

### <span id="android_base_24">24. AlertDialog、popupWindow、Activity 之间的区别？</span>
AlertDialog 与 PopupWindow 之间最本质的差异在于：

AlertDialog 是非阻塞式对话框；而PopupWindow 是阻塞式对话框。AlertDialog 弹出时，后台还可以做事情；PopupWindow 弹出时，程序会等待，在PopupWindow 退出前，程序一直等待，只有当我们调用了 dismiss() 方法的后，PopupWindow 退出，程序才会向下执行。我们在写程序的过程中可以根据自己的需要选择使用 Popupwindow 或者是 Dialog.   
两者最根本的区别在于有没有新建一个 window，PopupWindow 没有新建，而是通过 WMS 将 View 加到 DecorView；Dialog 是新建了一个 window (PhoneWindow)，相当于走了一遍 Activity 中创建 window 的流程。

### <span id="android_base_25">25. Application 和 Activity 的 Context 之间的区别？</span>
[https://www.jianshu.com/p/48772161b407](https://www.jianshu.com/p/48772161b407)
### <span id="android_base_26">26. Android 属性动画特性？</span>
[https://www.jianshu.com/p/e7c8f0af3c6f](https://www.jianshu.com/p/e7c8f0af3c6f)
### <span id="android_base_27">27. LinearLayout、RelativeLayout、FrameLayout 的特性对比及使用场景？</span>
[https://www.cnblogs.com/wgwyanfs/p/7288937.html](https://www.cnblogs.com/wgwyanfs/p/7288937.html)
### <span id="android_base_28">28. 对 SurfaceView 的了解？</span>
怎么理解SurfaceView呢？顾名思义就是Surface+View了，因此，这个东西有两重身份：首先，是一个View；其次还是一个带有Surface的View。首先聊聊View，View我们可以理解为视图了，android上的imageview，textview之类的，都可以理解为视图，这些视图可以直接在layout上规划。所以，SurfaceView，类似的，也可以直接在xml上规划。再来聊聊Surface，Surface可以理解为一块画布，应用可以在Surface上绘制自己的图像。对于视频而言，其本质，也是图像，只不过是在不断变化的图像，确切的说，是每秒变化30帧的图像（30fps）。
总结起来，SurfaceView本身是一个视图，可以在layout中布局，在这个视图中有一个画布是Surface，我们可以将图片绘制在这个Surface上。   
[https://www.jianshu.com/p/75135086fa2a](https://www.jianshu.com/p/75135086fa2a)
### <span id="android_base_29">29. Serializable 和 Parcelable 的区别？</span>
Serializable（Java自带）：
Serializable是序列化的意思，表示将一个对象转换成可存储或可传输的状态。序列化后的对象可以在网络上进行传输，也可以存储到本地。

Parcelable（android 专用）：
除了Serializable之外，使用Parcelable也可以实现相同的效果，
不过不同于将对象进行序列化，Parcelable方式的实现原理是将一个完整的对象进行分解，
而分解后的每一部分都是Intent所支持的数据类型，这样也就实现传递对象的功能了。
[https://www.jianshu.com/p/a60b609ec7e7](https://www.jianshu.com/p/a60b609ec7e7)
### <span id="android_base_30">30. Android 中数据存储方式有哪些？</span>
[https://www.jianshu.com/p/be711f87a18f](https://www.jianshu.com/p/be711f87a18f)
### <span id="android_base_31">31. 屏幕适配的处理技巧都有哪些?</span>
[https://www.jianshu.com/p/ec5a1a30694b](https://www.jianshu.com/p/ec5a1a30694b)
### <span id="android_base_32">32. Android 各个版本 API 的区别？</span>
[https://www.jianshu.com/p/3426528cc077](https://www.jianshu.com/p/3426528cc077)
### <span id="android_base_33">33. 动态权限适配方案，权限组的概念？</span>
[https://www.jianshu.com/p/dbe4d37731e6/](https://www.jianshu.com/p/dbe4d37731e6/)
### <span id="android_base_34">34. 为什么不能在子线程更新 UI？</span>
### <span id="android_base_35">35. ListView 图片加载错乱的原理和解决方案？</span>
### <span id="android_base_36">36. 对 RecycleView 的了解？</span>
### <span id="android_base_37">37. Recycleview 和 ListView 的区别？</span>
### <span id="android_base_38">38. RecycleView 实现原理？</span>
### <span id="android_base_39">39. Android Manifest 的作用与理解？</span>
### <span id="android_base_40">40. 多线程在 Android 中的使用？</span>

## 进阶

### <span id="android_advance_1">1. 画出 Android 的大体架构图</span>

   ![](https://i.loli.net/2018/11/04/5bde5e25b0aa9.png)

### <span id="android_advance_2">2. 低版本 SDK 如何使用高版本 API？</span>

### <span id="android_advance_3">3. AsyncTask 如何使用?</span>

### <span id="android_advance_4">4. AsyncTask 机制、原理及不足？</span>

### <span id="android_advance_5">5. 如果在 onStop() 的时候做了网络请求，onResume() 的时候怎么恢复？</span>

### <span id="android_advance_6">6. Handler 机制和底层实现？</span>

### <span id="android_advance_7">7. Handler、Thread、HandlerThread 区别？</span>

### <span id="android_advance_8">8. ThreadLocal 原理、实现及如何保证 Local 属性？</span>

### <span id="android_advance_9">9. 自定义 View 的流程？如何机型适配？</span>

### <span id="android_advance_10">10. 自定义 View 的时怎么获取 View 的大小？</span>

### <span id="android_advance_11">11. View 的绘制流程？</span>

### <span id="android_advance_12">12. View 的事件传递分发机制？</span>

### <span id="android_advance_13">13. requestLayout()，onLayout()，onDraw()，drawChild() 区别与联系？</span>

### <span id="android_advance_14">14. invalidate() 和 postInvalidate() 的区别？</span>

### <span id="android_advance_15">15. 如何计算一个 View 的嵌套层级？</span>

### <span id="android_advance_16">16. Android 动画框架及实现原理？</span>

### <span id="android_advance_17">17. 进程和 Application 的生命周期的关系？</span>

### <span id="android_advance_18">18. SpareArray 的实现原理？</span>

### <span id="android_advance_19">19. SharedPreferences 的实现眼里？是否进程同步？如何做到同步？</span>

### <span id="android_advance_20">20. ContentProvider 是如何实现数据共享的？</span>

### <span id="android_advance_21">21. ContentProvider 的权限管理？</span>

### <span id="android_advance_22">22. Android 系统为什么会设计 ContentProvider？</span>

### <span id="android_advance_23">23. Android 线程有没有上限？</span>

### <span id="android_advance_24">24. 怎么去除重复代码？</span>

### <span id="android_advance_25">25. Android 中开启摄像头的主要流程？</span>

### <span id="android_advance_26">26. 对 Bitmap 对象的了解？</span>

### <span id="android_advance_27">27. 图片加载原理？</span>

### <span id="android_advance_28">28. 图片压缩原理？</span>

### <span id="android_advance_29">29. 图片框架实现原理？LRUCache 原理？</span>

### <span id="android_advance_30">30. EventBus 实现原理？</span>

### <span id="android_advance_31">31. ButterKnife 实现原理？</span>

### <span id="android_advance_32">32. Volley 实现原理？</span>

### <span id="android_advance_33">33. okhttp 实现原理？</span>

### <span id="android_advance_34">34. 服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达？</span>

### <span id="android_advance_35">35. SQLite 数据库升级，数据迁移问题？</span>

### <span id="android_advance_36">36. 数据库框架对比和源码分析？</span>

### <span id="android_advance_37">37. CAS介绍，OAuth 授权机制？</span>

### <span id="android_advance_38">38. 谈谈你对安卓签名的理解</span>

### <span id="android_advance_39">39. App 是如何沙箱化，为什么要这么做？</span>

## 混合开发

### <span id="android_mixing_1">1. 混合开发的方式？各自优缺点和使用场景？</span>
### <span id="android_mixing_2">2. Hybird</span>
### <span id="android_mixing_3">3. React Native</span>
### <span id="android_mixing_4">4. Weex</span>
### <span id="android_mixing_5">5. Flutter</span>
### <span id="android_mixing_6">6. Dart</span>
### <span id="android_mixing_7">7. 快应用</span>

## Framework

### <span id="android_framework_1">1. 请介绍一下 NDK？</span>
### <span id="android_framework_2">2. 如何在 jni 中注册 native 函数，有几种注册方式?</span>
### <span id="android_framework_3">3. Android 进程分类？</span>
### <span id="android_framework_4">4. 谈谈对进程共享和线程安全的认识？</span>
### <span id="android_framework_5">5. 谈谈对多进程开发的理解以及多进程应用场景？</span>
### <span id="android_framework_6">6. 什么是协程？</span>
### <span id="android_framework_7">7. 逻辑地址与物理地址，为什么使用逻辑地址？</span>
### <span id="android_framework_8">8. Android 为每个应用程序分配的内存大小是多少？</span>
### <span id="android_framework_9">9. 进程保活的方式？</span>
### <span id="android_framework_10">10. 系统启动流程是什么？</span>
### <span id="android_framework_11">11. 一个应用程序安装到手机上的过程发生了什么？</span>
### <span id="android_framework_12">12. App 启动流程，从点击桌面开始（Activity 启动流程）？</span>
### <span id="android_framework_13">13. 什么是 AIDL？解决了什么问题？如何使用？</span>
### <span id="android_framework_14">14. Binder 机制及工作原理？</span>
### <span id="android_framework_15">15. App 中唤醒其他进程的实现方式？</span>
### <span id="android_framework_16">16. Activity、Window、View 三者的关系与区别？</span>
### <span id="android_framework_17">17. ApplicationContext 和 ActivityContext 的区别？</span>
### <span id="android_framework_18">18. ActivityThread，ActivityManagerService，WindowManagerService 的工作原理？</span>
### <span id="android_framework_19">19. PackageManagerService 的工作原理？</span>
### <span id="android_framework_20">20. PowerManagerService 的工作原理？</span>
### <span id="android_framework_21">21. 权限管理系统（底层的权限是如何进行 grant 的）？</span>

## 性能优化

### <span id="android_performance_1">1. 如何对 Android 应用进行性能分析以及优化?</span>
### <span id="android_performance_2">2. ANR 产生的原因是什么？怎么定位？</span>
### <span id="android_performance_3">3. OOM 是什么？怎么解决？是否可以 try catch？</span>
### <span id="android_performance_4">4. 内存泄露的解决方法？</span>
### <span id="android_performance_5">5. ddms 和 traceView 的使用？</span>
### <span id="android_performance_6">6. 性能优化如何分析 systrace？</span>
### <span id="android_performance_7">7. 用 IDE 如何分析内存泄漏？</span>
### <span id="android_performance_8">8. Java 多线程引发的性能问题，怎么解决？</span>
### <span id="android_performance_9">9. 启动页白屏、黑屏、太慢怎么解决？</span>
### <span id="android_performance_10">10. App 启动崩溃异常怎么捕捉？</span>
### <span id="android_performance_11">11. 如何保持应用的稳定性？</span>
### <span id="android_performance_12">12. RecyclerView 和 ListView 的性能对比？</span>
### <span id="android_performance_13">13. Bitmap 如何处理大图？如何预防 OOM？</span>
### <span id="android_performance_14">14. 如何缩小 Apk 的体积?</span>
### <span id="android_performance_15">15. 如何统计启动时长？</span>

##  Gradle

### <span id="android_gradle_1">1. Glide 源码解析</span>
### <span id="android_gradle_2">2. 对热修复和插件化的理解？</span>
### <span id="android_gradle_3">3. 插件化原理分析</span>
### <span id="android_gradle_4">4. 模块化实现（好处，原因）</span>
### <span id="android_gradle_5">5. 项目组件化的理解</span>
### <span id="android_gradle_6">6. 描述清点击 Android Studio 的 build 按钮后发生了什么？</span>

## Kotlin

### <span id="android_kotlin_1">1. 谈谈对 Kotlin 的理解</span>
### <span id="android_kotlin_2">2. 闭包和局部内部类的区别?</span>