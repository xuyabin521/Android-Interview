# Android 开发相关精华面试题

## 概述

该项目主要收集 Android 开发相关最具价值的面试题，已包含各个大厂的面试题及常见套路。

虽然不推荐大家刷题，这里仅供大家差缺补漏。所有的知识点还是重在自己理解，用自己的方式表达出来比较好。

该项目持续更新，欢迎大家 Star，如果有更优质的面试题欢迎联系我们提交。

## Java

### 基础

- [什么是面向对象（OOP）？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_1)
- [什么是多态？实现多态的机制是什么？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_2)
- [接口（Interface）与抽象类（Abstract Class）的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_3)
- [重写（Override）与重载（Overload）的区别?](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_4)
- [父类的静态方法能否被子类重写？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_5)
- [静态属性和静态方法是否可以被继承？是否可以被重写？为什么？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_6)
- [什么是内部类？内部类、静态内部类、局部内部类和匿名内部类的区别及作用？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_7)
- [== 和 equals() 和 hashCode() 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_8)
- [Integer 和 int 之间的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_9)
- [String 转换成 Integer 的方式及原理？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_10)
- [自动装箱实现原理？类型转换实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_11)
- [对 String 的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_12)
- [String 为什么要设计成不可变的？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_13)
- [final、finally 和 finalize 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_14)
- [static 关键字有什么作用？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_15)
- [列举 Java 的集合以及集合之间的继承关系?](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_16)
- [List、Set、Map 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_17)
- [ArrayList、LinkedList 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_18)
- [HashMap，HashTable，ConcurrentHashMap 实现原理以及区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_19)
- [HashSet 与 HashMap 怎么判断集合元素重复？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_20)
- [String、StringBuffer、StringBuilder 之间的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_21)
- [什么是序列化？怎么实现？有哪些方式？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_22)
- [对反射的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_23)
- [对注解的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_24)
- [对依赖注入的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_25)
- [对泛型的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_26)
- [泛型中 extends 和 super 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_27)
- [对 Java 的异常体系的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_28)
- [对解析与分派的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_29)
- [静态代理和动态代理的区别？有什么场景使用？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_30)
- [谈谈对 Java 状态机理解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_31)

### 线程与并发

- [线程和进程的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_1)
- [开启线程的三种方式](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_2)
- [如何正确的结束一个Thread?](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_3)
- [Thread 与 Runnable 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_4)
- [run() 与 start() 方法的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_5)
- [sleep() 与 wait() 方法的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_6)
- [wait 与 notify 关键字的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_7)
- [synchronized 关键字的用法、作用及实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_8)
- [volatile 关键字的用法、作用及实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_9)
- [transient 关键字的用法、作用及实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_10)
- [ReentrantLock、synchronized、volatile 之间的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_11)
- [什么是线程池，如何使用?](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_12)
- [多线程断点续传的实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_13)
- [什么是深拷贝和浅拷贝？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_14)
- [Java 中对象的生命周期？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_15)
- [对并发编程的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_thread_16)

###  JVM

- [简述 JVM 内存模型和内存区域？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_1)
- [简述垃圾回收器的工作原理？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_2)
- [如何判断对象的生死？垃圾回收算法？新生代，老生代？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_3)
- [哪些情况下的对象会被垃圾回收机制处理掉？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_4)
- [垃圾回收机制与调用 System.gc() 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_5)
- [强引用、软引用、弱引用、虚引用之间的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_6)
- [强引用设置为 null，会不会被回收？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_7)
- [简述 ClassLoader 类加载机制？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_8)
- [对双亲委派模型的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_9)
- [String a = "a"+"b"+"c" 在内存中创建几个对象？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_10)
- [对 Dalvik、ART 虚拟机的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_11)
- [对动态加载（OSGI）的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_12)
- [常见编码方式有哪些？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_13)
- [utf-8 编码中的中文占几个字节？int 型占几个字节？](https://github.com/xuyabin521/Android-Interview/blob/master/java/java.md#java_jvm_14)

## Android

### 基础

- [四大组件是什么？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_1)
- [Activity 的生命周期？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_2)
- [Activity 之间的通信方式？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_3)
- [Activity 各种情况下的生命周期？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_4)
- [横竖屏切换时 Activity 的生命周期](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_5)
- [前台切换到后台，然后再回到前台时 Activity 的生命周期](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_6)
- [弹出 Dialog 的时候按 Home 键时 Activity 的生命周期](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_7)
- [两个 Activity 之间跳转时的生命周期](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_8)
- [下拉状态栏时 Activity 的生命周期](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_9)
- [Activity 与 Fragment 之间生命周期比较？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_10)
- [Activity 的四种 LaunchMode（启动模式）的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_11)
- [Activity 状态保存与恢复？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_12)
- [Fragment 各种情况下的生命周期？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_13)
-  [Activity 和 Fragment 之间怎么通信， Fragment 和 Fragment 怎么通信？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_14)
- [Service 的生命周期？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_15)
- [Service 的启动方式？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_16)
- [Service 与 IntentService 的区别?](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_17)
- [Service 和 Activity 之间的通信方式？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_18)
- [对 ContentProvider 的理解？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_19)
- [ContentProvider、ContentResolver、ContentObserver 之间的关系？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_20)
- [对 BroadcastReceiver 的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_21)
- [广播的分类？使用方式和场景？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_22)
- [动态广播和静态广播有什么区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_23)
- [AlertDialog、popupWindow、Activity 之间的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_24)
- [Application 和 Activity 的 Context 之间的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_25)
- [Android 属性动画特性？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_26)
- [请列举 Android 中常见的布局（Layout）类型，并简述其用法，以及排版效率。
    LinearLayout、RelativeLayout、FrameLayout 的特性对比及使用场景？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_27)
- [对 SurfaceView 的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_28)
- [Serializable 和 Parcelable 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_29)
- [Android 中数据存储方式有哪些？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_30)
- [屏幕适配的处理技巧都有哪些?](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_31)
- [Android 各个版本 API 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_32)
- [动态权限适配方案，权限组的概念？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_33)
- [为什么不能在子线程更新 UI？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_34)
- [ListView 图片加载错乱的原理和解决方案？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_35)
- [对 RecycleView 的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_36)
- [Recycleview 和 ListView 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_37)
- [RecycleView 实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_38)
- [Android Manifest 的作用与理解？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_39)
- [多线程在 Android 中的使用？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_40)
- [区别 Animation 和 Animator 的用法，概述实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_base_41)

### 高级

- [画出 Android 的大体架构图](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_1)
- [低版本 SDK 如何使用高版本 API？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_2)
- [AsyncTask 如何使用?](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_3)
- [AsyncTask 机制、原理及不足？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_4)
- [如果在 onStop() 的时候做了网络请求，onResume() 的时候怎么恢复？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_5)
- [Handler 机制和底层实现？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_6)
- [Handler、Thread、HandlerThread 区别？
   Thread、Looper、MessageQueue、Handler、Message，每个类的功能是什么，这些类之间是什么关系？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_7)
- [ThreadLocal 原理、实现及如何保证 Local 属性？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_8)
- [自定义 View 的流程？如何机型适配？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_9)
- [自定义 View 的时怎么获取 View 的大小？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_10)
- [View 的绘制流程？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_11)
- [View 的事件传递分发机制？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_12)
- [requestLayout()，onLayout()，onDraw()，drawChild() 区别与联系？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_13)
- [invalidate() 和 postInvalidate() 的区别？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_14)
- [如何计算一个 View 的嵌套层级？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_15)
- [Android 动画框架及实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_16)
- [进程和 Application 的生命周期的关系？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_17)
- [SpareArray 的实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_18)
- [SharedPreferences 的实现眼里？是否进程同步？如何做到同步？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_19)
- [ContentProvider 是如何实现数据共享的？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_20)
- [ContentProvider 的权限管理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_21)
- [Android 系统为什么会设计 ContentProvider？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_22)
- [Android 线程有没有上限？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_23)
- [怎么去除重复代码？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_24)
- [Android 中开启摄像头的主要流程？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_25)
- [对 Bitmap 对象的了解？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_26)
- [图片加载原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_27)
- [图片压缩原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_28)
- [图片框架实现原理？LRUCache 原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_29)
- [EventBus 实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_30)
- [ButterKnife 实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_31)
- [Volley 实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_32)
- [okhttp 实现原理？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_33)
- [服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_34)
- [SQLite 数据库升级，数据迁移问题？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_35)
- [数据库框架对比和源码分析？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_36)
- [CAS介绍，OAuth 授权机制？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_37)
- [谈谈你对安卓签名的理解](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_38)
- [App 是如何沙箱化，为什么要这么做？](https://github.com/xuyabin521/Android-Interview/blob/master/android/android.md#android_advance_39)

### 混合开发

- 混合开发的方式？各自优缺点和使用场景？
- Hybird
- React Native
- Weex
- Flutter
- Dart
- 快应用

### Framework

- 请介绍一下 NDK？
- 如何加载 ndk 库？如何在 jni 中注册 native 函数，有几种注册方式?【猎豹移动】
- Android 进程分类？
- 谈谈对进程共享和线程安全的认识？
- 谈谈对多进程开发的理解以及多进程应用场景？
- 什么是协程？
- 逻辑地址与物理地址，为什么使用逻辑地址？
- Android 为每个应用程序分配的内存大小是多少？
- 进程保活的方式？
- 系统启动流程是什么？
- 一个应用程序安装到手机上的过程发生了什么？
- App 启动流程，从点击桌面开始（Activity 启动流程）？
- 什么是 AIDL？解决了什么问题？如何使用？
- Binder 机制及工作原理？
- App 中唤醒其他进程的实现方式？
- Activity、Window、View 三者的关系与区别？
- ApplicationContext 和 ActivityContext 的区别？
- ActivityThread，ActivityManagerService，WindowManagerService 的工作原理？
- PackageManagerService 的工作原理？
- PowerManagerService 的工作原理？
- 权限管理系统（底层的权限是如何进行 grant 的）？
- 操作系统中进程和线程有什么区别？系统在什么情况下会在用户态和内核态中切换？【猎豹移动】
- 如果一个 App 里面有多个进程存在，请列举你所知道的全部 IPC 方法。

### 性能优化

- 如何对 Android 应用进行性能分析以及优化?
- ANR 产生的原因是什么？怎么定位？
- OOM 是什么？怎么解决？是否可以 try catch？
- 内存泄露的解决方法？
- ddms 和 traceView 的使用？
- 性能优化如何分析 systrace？
- 用 IDE 如何分析内存泄漏？
- Java 多线程引发的性能问题，怎么解决？
- 启动页白屏、黑屏、太慢怎么解决？
- App 启动崩溃异常怎么捕捉？
    对于 Android App 闪退，可能有哪些原因？请针对每种情况简述分析过程。【猎豹移动】
- 如何保持应用的稳定性？
- RecyclerView 和 ListView 的性能对比？
- Bitmap 如何处理大图？如何预防 OOM？
- 如何缩小 Apk 的体积?
- 如何统计启动时长？

###  Gradle

- Gradle 源码解析
- 对热修复和插件化的理解？
- 插件化原理分析
- 模块化实现（好处，原因）
- 项目组件化的理解
- 描述清点击 Android Studio 的 build 按钮后发生了什么？

### Kotlin

- 谈谈对 Kotlin 的理解
- 闭包和局部内部类的区别?

## 网络技术

- [描述一次网络请求的流程?](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_1)
- [TCP 中 3 次握手和 4 次挥手的过程?](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_2)
- [TCP 与 UDP 的区别及应用?](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_3)
- [HTTP 协议](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_4)
- [HTTP 1.0 与 2.0 的区别](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_5)
- [HTTP 报文结构](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_6)
- [HTTP 与 HTTPS 的区别以及如何实现安全性](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_7)
- [HTTPS 原理](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_8)
- [谈谈你对 WebSocket 的理解](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_9)
- [WebSocket 与 socket 的区别](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_10)
- [视频加密传输](https://github.com/xuyabin521/Android-Interview/blob/master/network/network.md#quest_network_technological_process_11)

## 数据结构与算法

### 数据结构

- 简述常见的数据结构？
- 堆的结构？
- 树、B+ 树、二叉树、红黑树的了解？
- 二叉树的深度优先遍历和广度优先遍历？
- 堆和树的区别？
- 图的了解？

### 算法

- 排序算法有哪些？
- 最快的排序算法是哪个？
- 手写冒泡排序
- 手写快速排序
- 快速排序的过程、时间复杂度、空间复杂度
- 手写堆排序

### 常见算法问题

- 给阿里2万多名员工按年龄排序应该选择哪个算法？
- GC算法(各种算法的优缺点以及应用场景)
- 蚁群算法与蒙特卡洛算法
- 子串包含问题(KMP 算法)写代码实现
- 一个无序，不重复数组，输出N个元素，使得N个元素的和相加为M，给出时间复杂度、空间复杂度。手写算法
- 万亿级别的两个URL文件A和B，如何求出A和B的差集C(提示：Bit映射->hash分组->多文件读写效率->磁盘寻址以及应用层面对寻址的优化)
- 两个不重复的数组集合中，求共同的元素。
- 两个不重复的数组集合中，这两个集合都是海量数据，内存中放不下，怎么求共同的元素？
- 一个文件中有100万个整数，由空格分开，在程序中判断用户输入的整数是否在此文件中。说出最优的方法
- 一张Bitmap所占内存以及内存占用的计算
- 2000万个整数，找出第五十大的数字？
- 求1000以内的水仙花数以及40亿以内的水仙花数
- 烧一根不均匀的绳，从头烧到尾总共需要1个小时。现在有若干条材质相同的绳子，问如何用烧绳的方法来计时一个小时十五分钟呢？
- 5枚硬币，2正3反如何划分为两堆然后通过翻转让两堆中正面向上的硬8币和反面向上的硬币个数相同
- 时针走一圈，时针分针重合几次

## 设计模式与架构

### 设计模式

- 谈谈你对 Android 设计模式的理解
- 项目中常用的设计模式有哪些？
- 手写生产者-消费者模式？
- 手写观察者模式？
- 适配器模式、装饰者模式、外观模式的异同？

### 架构

- MVC、MVP、MVVM 原理和区别？
  请画出 MVC、MVP 的差异？【猎豹移动】
- 对 RxJava 的理解，功能与原理，优缺点？
- 从 0 设计一款 App 整体架构，如何去做？
- Fragment 如果在 Adapter 中使用应该如何解耦？
- 对于应用更新这块是如何做的？(解答：灰度，强制更新，分区域更新)？
- 实现一个 Json 解析器（可以通过正则提高速度）？

## 人事相关

- [请简单做个自我介绍？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_1)
- [为什么离开上家公司？您在前一家公司的离职原因是什么？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_2)
- [为什么要做 xxx 岗位（出现所学专业与求职岗位不同时提问）?](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_3)
- [讲一个你认为做的最好的项目/案例](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_4)
- [你应聘该岗位的优势是什么？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_5)
- [你上家公司的薪水/期望的薪金？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_6)
- [你对薪资的要求？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_7)
- [谈谈你对跳槽的看法？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_8)
- [对待加班看法？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_9)
- [自己最擅长的技术点，最感兴趣的技术领域和技术点，做了那些东西？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_10)
- [自己的优点和缺点是什么？并举例说明？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_11)
- [你朋友对你的评价？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_12)
- [说下项目中遇到的棘手问题，包括技术，交际和沟通？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_13)
  项目中遇到最大的困难是什么？如何解决的？
- [在五年的时间内，你的职业规划？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_14)
- [给你一个项目，你怎么看待他的市场和技术的关系？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_15)
- [你一般喜欢从什么渠道获取技术信息和提高自己的能力？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_16)
  你的学习方法是什么样的？实习过程中如何学习？实习项目中遇到的最大困难是什么以及如何解决的？
- [如果实际工作后发现自己不适合这个职位怎么办？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_17)
  如果通过这次面试我们单位录用了你，但工作一段时间却发现你根本不适合这个职位，你怎么办？
- [工作上与领导意见不同时，怎么办？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_18)
- [如果你的主管抢了你的功劳你该怎样？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_19)
- [若上司在公开会议上误会你了，该如何解决？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_20)
- [工作中你难以和同事、上司相处，你该怎么办？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_21)
- [因成绩比较突出，受同事们孤立你怎么看？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_22)
- [你和别人发生过争执吗？你是怎样解决的？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_23)
- [如果工作失误，给公司造成经济损失，你该怎么办？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_24)
- [你对于我们公司了解多少？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_25)
- [你为什么愿意到我们公司来工作？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_26)
- [你能为我们公司带来什么？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_27)
- [你最擅长的技术点，最感兴趣的技术领域和技术点？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_28)
- [说说你对行业、技术发展趋势的看法？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_29)
- [理想中的工作环境是什么？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_30)
- [说说你的家庭？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_31)
- [就你申请的这个职位，你认为你还欠缺什么？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_32)
- [你做过的哪件事最令自己感到骄傲？说一件最能证明你能力的事情？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_33)
- [对这项工作，你有哪些可预见的困难？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_34)
- [如果被录用，你将怎样开展工作？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_35)
- [希望与什么样的上级共事？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_36)
- [你工作经验欠缺，如何能胜任这项工作？ ](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_37)
- [如果你在这次面试中没有被录用，你怎么打算？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_38)
- [除了本公司外，还应聘了哪些公司？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_39)
- [你还要什么了解和要问的吗？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_40)
- [实习过程中周围同事/同学有哪些值得学习的地方？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_41)
- [是否可以实习，可以实习多久？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_42)
- [实习过程中做了什么，有什么产出？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_43)
- [公司实习最大的收获是什么？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_44)
- [评价下自己，评价下自己的技术水平，个人代码量如何？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_45)
- [当前的 offer 状况；如果 BATH 都给了offer 该如何选？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_46)
- [你对一份工作更看重哪些方面？平台，技术，氛围，城市，还是 money？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_47)
- [假如你晚上要去送一个出国的同学去机场，可单位临时有事非你办不可，你怎么办？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_48)
- [你看中公司的什么？或者公司的那些方面最吸引你？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_49)
- [讲一件你印象最深的一件事情？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_50)
- [介绍你做过的哪些项目，介绍一个你影响最深的项目？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_51)
- [你做过的哪件事最令自己感到骄傲？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_52)
- [都使用过哪些框架、平台？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_53)
- [都使用过哪些自定义控件？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_54)
- [项目中用了哪些开源库，如何避免因为引入开源库而导致的安全性和稳定性问题？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_55)
- [有没有什么开源项目？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_56)
- [研究比较深入的领域有哪些？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_57)
- [对业内信息的关注渠道有哪些？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_58)
- [业余都有哪些爱好？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_59)
- [最近都读哪些书？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_60)
- [你的梦想是什么？](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_61)

## 常见套路

如果有遇到以下这些情况，你可以继续投简历：

- [我们 xx 总不在，会叫 hr 联系你，你先回去等通知](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_62)
- [面试叫你带上以往作品（工作成绩需要以往作品展示的除外，如：ui）然后面试官一直问你方案是怎么做的](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_63)
- [遇到面试官敷衍随便问问题](https://github.com/xuyabin521/Android-Interview/blob/master/other/other.md#other_64)

## 成员

- [singwhatiwanna](https://github.com/singwhatiwanna)
- [Daimhim](https://github.com/Daimhim)
- [Jeanboy](https://github.com/xuyabin521/Android-ReadTheFuckingSourceCode)
- [ljingya](https://github.com/ljingya)
- [沐小晨曦](https://github.com/Omooo)
- [scofeildsun](https://github.com/scofeildsun)
- [Mr.S](https://github.com/shishaoyan)
- [shulianpang](https://github.com/shulianpang)

同时欢迎大家加入我们一起整理收集，整理面试题不仅仅是对自己技术的检验，也可以帮助大家，为开源做一下贡献，期待您的加入。（申请加入请联系： [Jeanboy](https://github.com/xuyabin521/Android-ReadTheFuckingSourceCode)）
