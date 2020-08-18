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
### <span id="android_base_6">6. 前台切换到后台，然后再回到前台时 Activity 的生命周期</span>
### <span id="android_base_7">7. 弹出 Dialog 的时候按 Home 键时 Activity 的生命周期</span>
### <span id="android_base_8">8. 两个 Activity 之间跳转时的生命周期</span>
### <span id="android_base_9">9. 下拉状态栏时 Activity 的生命周期</span>
### <span id="android_base_10">10. Activity 与 Fragment 之间生命周期比较？</span>
### <span id="android_base_11">11. Activity 的四种 LaunchMode（启动模式）的区别？</span>
### <span id="android_base_12">12. Activity 状态保存与恢复？</span>
### <span id="android_base_13">13. Fragment 各种情况下的生命周期？</span>
### <span id="android_base_14">14. Activity 和 Fragment 之间怎么通信， Fragment 和 Fragment 怎么通信？</span>

	Activity 传值给 Fragment：通过 Bundle 对象来传递，Activity 中构造 bundle 数据包，调用 Fragment 对象的 `setArguments(Bundle b)` 方法，Fragment 中使用 `getArguments()` 方法获取 Activity 传递过来的数据包取值。
	
	Fragment 传值给 Activity：在 Fragment 中定义一个内部回调接口，Activity 实现该回调接口， Fragment 中获取 Activity 的引用，调用 Activity 实现的业务方法。接口回调机制式 Java 不同对象之间数据交互的通用方法。
	
	Fragment 传值给 Fragment：一个 Fragment 通过 Activity 获取到另外一个 Fragment 直接调用方法传值。

### <span id="android_base_15">15. Service 的生命周期？</span>
### <span id="android_base_16">16. Service 的启动方式？</span>
### <span id="android_base_17">17. Service 与 IntentService 的区别?</span>
### <span id="android_base_18">18. Service 和 Activity 之间的通信方式？</span>

- 通过 Binder 对象
- 通过 Broadcast（广播）的形式

### <span id="android_base_19">19. 对 ContentProvider 的理解？</span>
### <span id="android_base_20">20. ContentProvider、ContentResolver、ContentObserver 之间的关系？</span>
### <span id="android_base_21">21. 对 BroadcastReceiver 的了解？</span>
### <span id="android_base_22">22. 广播的分类？使用方式和场景？</span>
### <span id="android_base_23">23. 动态广播和静态广播有什么区别？</span>

- 动态的比静态的安全
- 静态在 App 启动的时候就初始化了，动态使用代码初始化
- 静态需要配置，动态不需要
- 生存期，静态广播的生存期可以比动态广播的长很多
- 优先级动态广播的优先级比静态广播高

### <span id="android_base_24">24. AlertDialog、popupWindow、Activity 之间的区别？</span>
### <span id="android_base_25">25. Application 和 Activity 的 Context 之间的区别？</span>
### <span id="android_base_26">26. Android 属性动画特性？</span>
### <span id="android_base_27">27. LinearLayout、RelativeLayout、FrameLayout 的特性对比及使用场景？</span>
### <span id="android_base_28">28. 对 SurfaceView 的了解？</span>
### <span id="android_base_29">29. Serializable 和 Parcelable 的区别？</span>
### <span id="android_base_30">30. Android 中数据存储方式有哪些？</span>
### <span id="android_base_31">31. 屏幕适配的处理技巧都有哪些?</span>
### <span id="android_base_32">32. Android 各个版本 API 的区别？</span>
### <span id="android_base_33">33. 动态权限适配方案，权限组的概念？</span>
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