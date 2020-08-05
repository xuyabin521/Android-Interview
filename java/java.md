# Java

## 基础

### <span id="java_1">1. 什么是面向对象（OOP）？</span>

面向对象编程是使用类，对象，继承性，多态性，封装性和抽象的一种程序设计方法。

首先我们要区分一下“基于对象”和“面向对象”的区别。

1. 基于对象，通常指的是对数据的封装，以及提供一组方法对封装过的数据操作。
2. 面向对象，则在基于对象的基础上增加了多态性。所谓多态，就是可以用统一的方法对不同的对象进行同样的操作。

[什么是面向对象（OOP）？](https://www.jianshu.com/p/7a5b0043b035)

### <span id="java_2">2. 什么是多态？实现多态的机制是什么？</span>

多态即：事物在运行过程中存在不同的状态。多态可以分为编译时多态和运行时多态，编译时多态是指方法的重载，运行时多态是指方法的重写。

对于运行时多态需要满足以下三个条件：

1. 要有继承关系
2. 子类重写父类方法
3. 父类对象的引用指向子类对象（SuperClass class = new ChildClass() ）

那么多态实现的机制是什么呢？

其实就是依靠静态分派和动态分派。

静态分派即在编译期间就能完全确定，在类加载的解析阶段就会把所涉及的符号引用转化为可确定的直接引用，不会延迟到运行期再去完成，典型的例子就是方法重载。

动态分派是指在运行期间才能确定变量的实际类型，典型的例子就是方法的重写。只有在运行期间，根据对实例化子类的不同，调用不同子类中重写的方法。

参考：[多态性实现机制——静态分派与动态分派](https://www.jianshu.com/p/1976b01c07d2)

### <span id="java_3">3. 接口（Interface）与抽象类（Abstract Class）的区别？</span>

抽象类是一个可同时包含具体方法和抽象方法(方法未被实现)的类。抽象方法必须被该抽象类的子类实现。抽象类是可以继承的。

接口像是描述类的一张蓝图或者说是类的一种契约，它包含了许多空方法，这代表着它的所有的子类都应该拥有共同点。它的子类应该提供这些空方法的具体实现。一 个类需要用 implements 来实现接口，接口可以用 extends 来继承其他接口。

[接口（Interface）与抽象类（Abstract Class）的区别？](https://www.jianshu.com/p/c4f023d02f0c)

### <span id="java_4"> 4. 重写（Override）与重载（Overload）的区别?</span>

1. 覆盖是子类与父类之间的关系，是一种垂直关系；重载是同一个类中方法之间的关系，是水平关系
2. 覆盖只能由一个方法或者只能由一对方法产生关系；重载是多个方法之间的关系
3. 覆盖要求参数列表要相同；重载要求参数列表不同
4. 覆盖关系中，调用方法体是根据对象的类型（对象对应存储空间类型）决定，重载是根据调用的时候实参表和形参表来选择方法

### <span id="java_5">5. 父类的静态方法能否被子类重写？</span>

严格来说，不存在静态方法的重写，当一个子类继承父类时，写同样的方法时，只是将父类的静态方法隐藏。

### <span id="java_6">6. 静态属性和静态方法是否可以被继承？是否可以被重写？为什么？</span>
静态属性和静态方法可以被继承不可以被重写，静态属性和方法的继承但是并不是严格意义上的继承，静态属性和方法属于一个类的，并不属于对象的，既是类不实例化成对象也是可以正常使用静态方法和属性的，静态属性和方法在内存中一般只存在一份。
### <span id="java_7">7. 什么是内部类？内部类、静态内部类、局部内部类和匿名内部类的区别及作用？</span>
在 Java 中，可以将一个类定义在另一个类里面或者一个方法里面，这样的类称为内部类。广泛意义上的内部类一般来说包括这四种：成员内部类、局部内部类、匿名内部类和静态内部类。下面就先来了解一下这四种内部类的用法。
成员内部类是最普通的内部类，它的定义为位于另一个类的内部；
局部内部类是定义在一个方法或者一个作用域里面的类，它和成员内部类的区别在于局部内部类的访问仅限于方法内或者该作用域内；
匿名内部类应该是平时我们编写代码时用得最多的，在编写事件监听的代码时使用匿名内部类不但方便，而且使代码更加容易维护；
静态内部类也是定义在另一个类里面的类，只不过在类的前面多了一个关键字static。静态内部类是不需要依赖于外部类的，这点和类的静态成员属性有点类似，并且它不能使用外部类的非static成员变量或者方法，这点很好理解，因为在没有外部类的对象的情况下，可以创建静态内部类的对象，如果允许访问外部类的非static成员就会产生矛盾，因为外部类的非static成员必须依附于具体的对象。
### <span id="java_8">8. == 和 equals() 和 hashCode() 的区别？</span>

== 和 equals 都是比较，弄清楚 == 和 equals 分别比较的是什么（内存地址，还是内存地址中的内容），自然就知道了==和equals有什么区别。
java对象都存在于内存中，要清楚我们要比较的到底是内存的地址，还是内存中的值。

先看几段代码：
```
String s1 = "AAAAA";
String s2 = "AAAAA";
System.out.println(s1 == s2);               // true
System.out.println(s1.equals(s2));          // true
```
```
String s3 = new String("BBBBB");
String s4 = new String("BBBBB");
System.out.println(s3 == s4);               // false
System.out.println(s3.equals(s4));          // true
```
```
Integer A = new Integer(20);
Integer B = new Integer(20);
System.out.println(A == B);                 // false
System.out.println(A.equals(B));            // true
```

我们再分别看看String类和Integer类中equals方法的源码：
```
public boolean equals(Object anObject) {
	if (this == anObject) {
		return true;
	}
	if (anObject instanceof String) {
		String anotherString = (String)anObject;
		int n = value.length;
		if (n == anotherString.value.length) {
			char v1[] = value;
			char v2[] = anotherString.value;
			int i = 0;
			while (n-- != 0) {
				if (v1[i] != v2[i])
					return false;
				i++;
			}
			return true;
		}
	}
	return false;
}
```
```
public boolean equals(Object obj) {
	if (obj instanceof Integer) {
		return value == ((Integer)obj).intValue();
	}
	return false;
}
```

从String类和Integer类的equals方法中，可以看到，equals的比较，最后还是运用!=或者==运算符来进行比较。**而且比较的，都是对象中的值。**

---

Java中所有的类，都是从Object继承而来，也就是说，Object是所有Java类的基类。

Object类中的函数并不多，equals方法就是其中的一个，看看equals在Object类中的源码：
```
public boolean equals(Object obj) {
    return (this == obj);
}
```
从Object源码中可以看到，equals方法最终调用的是\==进行比较的，那这里的\==比较的是什么呢？

**答：比较的是这个东西——java.lang.Object@15db9742。**

这是什么？

**答：这是Object类中toString方法的返回值。**

那再来看看Object类中toString方法的源码：
```
public String toString() {
    return getClass().getName() + "@" + Integer.toHexString(hashCode());
}
```

Object类toString方法返回的这一串东西java.lang.Object@15db9742是一个对象的类名和hash值，**这个hash值可以理解为内存地址**。

所以Objcet类中equals方法，比较的是两个内存地址，而不是内存地址中的值。

---

**结论：**

**equals和==都是进行比较操作，但是一个对象可比较的东西有很多，比如内存地址，内存地址中的值，但具体比较的是内存地址的值，还是内存地址中的值，就自己去看具体类的eaquals方法了。**

### <span id="java_9">9. Integer 和 int 之间的区别？</span>
Integer是类，int是基本数据类型。
### <span id="java_10">10. String 转换成 Integer 的方式及原理？</span>
使用的parseInt进行转换的，内部根据ASCII进行逐字对比。
### <span id="java_11">11. 自动装箱实现原理？类型转换实现原理？</span>
自动装箱就是Java自动将原始类型值转换成对应的对象，比如将int的变量转换成Integer对象，这个过程叫做装箱，反之将Integer对象转换成int类型值，这个过程叫做拆箱。

### <span id="java_12">12. 对 String 的了解？</span>
[https://www.jianshu.com/p/80d36d75ac94](https://www.jianshu.com/p/80d36d75ac94)
### <span id="java_13">13. String 为什么要设计成不可变的？</span>
[https://blog.csdn.net/renfufei/article/details/16808775](https://blog.csdn.net/renfufei/article/details/16808775)
### <span id="java_14">14. final、finally 和 finalize 的区别？</span>

1. final: 修饰变量，方法，类； 修饰变量时表明这对象的值不可变，你不能为这个变量赋一个新的值，或者这样说：对基本类型而言，你不能改变其数值，对于引用，你不能将其指向一个新的引用（而引用自身是可以改变的）。 修饰方法时表明我们希望把这个方法锁定，以防止任何继承类修改它的含义，这样会确保在继承中，我们的 final 方法的行为不会改变，并且不会被覆盖。使用 final 方法的另一个考虑是效率问题：在 Java 早期的时候，遇到 final 方法，编译器会将此方法调用转为内嵌调用，如此一来以减小方法调用产生的开销。 修饰类的时候表明你不打算继承该类，而且也不允许别人这样做。
2. finally: 是异常处理中进行收场处理的代码块，比如关闭一个数据库连接，清理一些资源占用的问题。不管有没有异常被捕获，finally 子句中的代码都会被执行。
3. finalize: finalize 出现的原因在于，我们一定需要进行清理动作。Java 没有用于释放对象的，如同 C++ 里的 delete 调用，的方法，而是使用垃圾回收器（GC）帮助我们释放空间。当垃圾回收器准备释放对象占用的存储空间的时候，将首先调用其 finalize() 方法。

### <span id="java_15">15. static 关键字有什么作用？</span>

static 是 Java 里的非访问修饰符，它可以用来创建类方法和类变量。

当修饰一个变量的时候，此变量就成了独立于对象的静态变量，无论一个类实例化了多少个对象，这个类只有一份这个静态变量的拷贝，所以 static 修饰的变量，即静态变量，也被叫做类变量。一个局部变量不能被声明为 static 变量。

当修饰一个方法的时候，此方法就成了独立于对象的静态方法，静态方法不能使用类的非静态变量，因为静态方法和静态变量先于非静态的其他成员初始化，静态方法先出来，然后才是非静态的，所以明白这个顺序很重要。静态方法从参数列表得到数据，然后计算这些数据。

### <span id="java_16">16. 列举 Java 的集合以及集合之间的继承关系?</span>
[https://blog.csdn.net/github_37130188/article/details/95110737](https://blog.csdn.net/github_37130188/article/details/95110737)
### <span id="java_17">17. List、Set、Map 的区别？</span>
1. List是一个继承于Collection的接口，即List是集合中的一种。List是有序的队列，List中的每一个元素都有一个索引；第一个元素的索引值是0，往后的元素的索引值依次+1。和Set不同，List中允许有重复的元素。实现List接口的集合主要有：ArrayList、LinkedList、Vector、Stack。
2. Set是一个继承于Collection的接口，Set是一种不包括重复元素的Collection。它维持它自己的内部排序，所以随机访问没有任何意义。与List一样，它同样运行null的存在但是仅有一个。由于Set接口的特殊性，所有传入Set集合中的元素都必须不同，关于API方面。Set的API和Collection完全一样。实现了Set接口的集合有：HashSet、TreeSet、LinkedHashSet、EnumSet。
3. Map与List、Set接口不同，它是由一系列键值对组成的集合，提供了key到Value的映射。在Map中它保证了key与value之间的一一对应关系。也就是说一个key对应一个value，所以它不能存在相同的key值，当然value值可以相同。实现map的集合有：HashMap、HashTable、TreeMap、WeakHashMap。

	[https://www.cnblogs.com/jxxblogs/p/11561629.html](https://www.cnblogs.com/jxxblogs/p/11561629.html)
	
### <span id="java_18">18. ArrayList、LinkedList 的区别？</span>

- ArrayList 实现了可变大小的数组。它允许 null。ArrayList 没有同步。增删慢，查询快。
- LinkedList 实现了 List 接口，允许 null 元素。此外 LinkedList 提供额外的 get，remove，insert 方法在 LinkedList 的首部或尾部。LinkedList 不是同步的（不是线程安全）。LinkedList 增删快，查询慢。
实现线程安全方式如下：
```Java
List list = Collections.synchronizedList(new LinkedList(...)); 
```

### <span id="java_19">19. HashMap，HashTable，ConcurrentHashMap 实现原理以及区别？</span>
[https://www.cnblogs.com/one-apple-pie/p/10466755.html](https://www.cnblogs.com/one-apple-pie/p/10466755.html)
### <span id="java_20">20. HashSet 与 HashMap 怎么判断集合元素重复？</span>
HashMap中判断元素是否相同主要有两个方法，一个是判断key是否相同，一个是判断value是否相同

HashSet不能添加重复的元素，当调用add（Object）方法时候，
首先会调用Object的hashCode方法判hashCode是否已经存在，如不存在则直接插入元素；

如果已存在则调用Object对象的equals方法判断是否返回true，如果为true则说明元素已经存在，如为false则插入元素。

发现HashSet竟然是借助HashMap来实现的，利用HashMap中Key的唯一性，来保证HashSet中不出现重复值。

从这段代码中可以看出，HashMap中的Key是根据对象的hashCode() 和 euqals()来判断是否唯一的。

结论：为了保证HashSet中的对象不会出现重复值，在被存放元素的类中必须要重写hashCode()和equals()这两个方法。
### <span id="java_21">21. String、StringBuffer、StringBuilder 之间的区别？</span>
1. String的值是不可变的，这就导致每次对String的操作都会生成新的String对象，不仅效率低下，而且浪费大量优先的内存空间 
2. StringBuffer是可变类，和线程安全的字符串操作类，任何对它指向的字符串的操作都不会产生新的对象。每个StringBuffer对象都有一定的缓冲区容量，当字符串大小没有超过容量时，不会分配新的容量，当字符串大小超过容量时，会自动增加容量 ，线程安全，多线程操作字符串。
3. StringBuilder可变类，速度更快，线程不安全， 单线程操作字符串。

	[https://blog.csdn.net/itchuxuezhe_yang/article/details/89966303](https://blog.csdn.net/itchuxuezhe_yang/article/details/89966303)
	
### <span id="java_22">22. 什么是序列化？怎么实现？有哪些方式？</span>

序列化是一种将对象转换为字节流的过程，目的是为了将该对象存储到内存中，等后面再次构建该对象时可以获取到该对象先前的状态及数据信息。

Java 中，只有一种方式可以实现序列化，只需要实现 Serializable 接口。

在 Android 中，还有另外一种实现序列化的方式,实现 Parcelable，这个是 Android 独有的一种序列化方方式,相比较 Serializable，Parcelable 需要提供大量的模板代码，较为繁琐，但是效率比 Serializable 高出不少，因为 Serializable 实现的序列化利用反射，可能会进行频繁的IO操作，所以消耗比较大。而 Parcelable 则是在内存中进行序列化。

所以这里推荐的是：

- 内存序列化优先选择 Parcelable。
- 存储到设备优先选择 Serializable(这里推荐使用 json 方式加密保存在本地，比较简单)

### <span id="java_23">23. 对反射的了解？</span>
[https://www.jianshu.com/p/61bd7c105082](https://www.jianshu.com/p/61bd7c105082)
### <span id="java_24">24. 对注解的了解？</span>
[https://blog.csdn.net/qq_29229567/article/details/93881883](https://blog.csdn.net/qq_29229567/article/details/93881883)
### <span id="java_25">25. 对依赖注入的了解？</span>
[https://www.cnblogs.com/alltime/p/6729295.html](https://www.cnblogs.com/alltime/p/6729295.html)
### <span id="java_26">26. 对泛型的了解？</span>
[https://zhuanlan.zhihu.com/p/79357469](https://zhuanlan.zhihu.com/p/79357469)
### <span id="java_27">27. 泛型中 extends 和 super 的区别？</span>
[https://www.jianshu.com/p/6ce3ee5fd93b](https://www.jianshu.com/p/6ce3ee5fd93b)
### <span id="java_28">28. 对 Java 的异常体系的了解？</span>
[https://www.jianshu.com/p/d227599404ee](https://www.jianshu.com/p/d227599404ee)
### <span id="java_29">29. 对解析与分派的了解？</span>
[https://www.jianshu.com/p/44790a602e11](https://www.jianshu.com/p/44790a602e11)
### <span id="java_30">30. 静态代理和动态代理的区别？有什么场景使用？</span>
[https://www.jianshu.com/p/c17350962f29](https://www.jianshu.com/p/c17350962f29)
### <span id="java_31">31. 谈谈对 Java 状态机理解？</span>
[https://zhuanlan.zhihu.com/p/97442825](https://zhuanlan.zhihu.com/p/97442825)

## 线程与并发

### <span id="java_thread_1">1. 线程和进程的区别？</span>
	根本区别：进程是操作系统资源分配的基本单位，而线程是任务调度和执行的基本单位
	
	在开销方面：每个进程都有独立的代码和数据空间（程序上下文），程序之间的切换会有较大的开销；线程可以看做轻量级的进程，同一类线程共享代码和数据空间，每个线程都有自己独立的运行栈和程序计数器（PC），线程之间切换的开销小。
	
	所处环境：在操作系统中能同时运行多个进程（程序）；而在同一个进程（程序）中有多个线程同时执行（通过CPU调度，在每个时间片中只有一个线程执行）
	
	内存分配方面：系统在运行的时候会为每个进程分配不同的内存空间；而对线程而言，除了CPU外，系统不会为线程分配内存（线程所使用的资源来自其所属进程的资源），线程组之间只能共享资源。
	
	包含关系：没有线程的进程可以看做是单线程的，如果一个进程内有多个线程，则执行过程不是一条线的，而是多条线（线程）共同完成的；线程是进程的一部分，所以线程也被称为轻权进程或者轻量级进程。
### <span id="java_thread_2">2. 开启线程的三种方式</span>
[https://www.cnblogs.com/lgjava/p/9997126.html](https://www.cnblogs.com/lgjava/p/9997126.html)
### <span id="java_thread_3">3. 如何正确的结束一个Thread?</span>
[https://www.cnblogs.com/lukelook/p/10001298.html](https://www.cnblogs.com/lukelook/p/10001298.html)
### <span id="java_thread_4">4. Thread 与 Runnable 的区别？</span>
[https://blog.csdn.net/dfshsdr/article/details/92432519](https://blog.csdn.net/dfshsdr/article/details/92432519)
### <span id="java_thread_5">5. run() 与 start() 方法的区别？</span>
	启动一个线程需要调用 Thread 对象的 start() 方法
	调用线程的 start() 方法后，线程处于可运行状态，此时它可以由 JVM 调度并执行，这并不意味着线程就会立即运行
	run() 方法是线程运行时由 JVM 回调的方法，无需手动写代码调用
	直接调用线程的 run() 方法，相当于在调用线程里继续调用方法，并未启动一个新的线程
### <span id="java_thread_6">6. sleep() 与 wait() 方法的区别？</span>
	1.相同点：
	（1）这两个方法都能使线程进入阻塞状态
	2.不同点：
	（1）sleep()方法是Thread类中的静态方法；而wait()方法是Object类中的方法；
	（2）sleep()方法可以在任何地方调用；而wait()方法只能在同步代码块或同步方法中使用(即使用synchronized关键字修饰的)；
	（3）这两个方法都在同步代码块或同步方法中使用时，sleep()方法不会释放同步监视器；而wait()方法则会释放同步监视器；
### <span id="java_thread_7">7. wait 与 notify 关键字的区别？</span>
[https://blog.csdn.net/github_37130188/article/details/97637072](https://blog.csdn.net/github_37130188/article/details/97637072)
### <span id="java_thread_8">8. synchronized 关键字的用法、作用及实现原理？</span>
synchronized关键字是解决多个线程之间访问资源的同步性，可保证所修饰的代码块在任意时刻只有一个线程执行
[https://blog.csdn.net/smarthunya/article/details/104359878](https://blog.csdn.net/smarthunya/article/details/104359878)
### <span id="java_thread_9">9. volatile 关键字的用法、作用及实现原理？</span>
[https://www.cnblogs.com/sunleejon/p/12499518.html](https://www.cnblogs.com/sunleejon/p/12499518.html)
### <span id="java_thread_10">10. transient 关键字的用法、作用及实现原理？</span>
	transient关键字的作用，在已实现序列化的类中，有的变量不需要保存在磁盘中，就要transient关键字修饰，如银行卡密码等，就这个作用------在已序列化的类中使变量不序列化
### <span id="java_thread_12">11. ReentrantLock、synchronized、volatile 之间的区别？</span>
[https://blog.csdn.net/weixin_43946462/article/details/107425373](https://blog.csdn.net/weixin_43946462/article/details/107425373)
### <span id="java_thread_13">12. 什么是线程池，如何使用?</span>
[https://www.cnblogs.com/baxianhua/p/9300952.html](https://www.cnblogs.com/baxianhua/p/9300952.html)
### <span id="java_thread_14">13. 多线程断点续传的实现原理？</span>
[https://blog.csdn.net/cledwyn/article/details/88323577](https://blog.csdn.net/cledwyn/article/details/88323577)
### <span id="java_thread_15">14. 什么是深拷贝和浅拷贝？</span>
[https://www.jianshu.com/p/94dbef2de298](https://www.jianshu.com/p/94dbef2de298)
### <span id="java_thread_15">15. Java 中对象的生命周期？</span>
[https://www.jianshu.com/p/780f4c133c52](https://www.jianshu.com/p/780f4c133c52)
### <span id="java_thread_16">16. 对并发编程的了解？</span>
[https://www.cnblogs.com/mrxiab/p/10676116.html](https://www.cnblogs.com/mrxiab/p/10676116.html)

## JVM

### <span id="java_jvm_1">1. 简述 JVM 内存模型和内存区域？</span>

**内存模型：**

Java 内存模型规定了所有的变量都是存储在主内存中。每条线程还有自己的工作内存，线程的工作内存中保存了该线程使用到的变量的主内存副本拷贝，线程对变量的所有操作都必须在工作内存中进行，而不能直接读写主内存中的变量。不同的线程之间也无法直接访问对方工作内存中的变量，线程间变量值的传递均需要通过主内存来完成。

![](https://i.loli.net/2018/11/05/5bdfcb13471a8.jpg)

**内存区域：**

![](https://i.loli.net/2018/11/05/5bdfce578c055.jpg)

内存区域可以分为以下几块：

- 程序计数器

  程序计数器是一块较小的内存空间，它可以看作是当前线程所执行的字节码的行号指示器。如果线程正在执行的是一个 Java 方法，这个计数器记录的是正在执行的虚拟机字节码指令的地址；如果正在执行的是 Native 方法，这个计数器值为空。此内存区域是唯一一个没有规定任何 OOM 的区域。

- 虚拟机栈

  虚拟机栈描述的是 Java 方法执行的内存模型：每个方法在执行的同时都会创建一个栈桢用于存储局部变量表、操作数栈、动态链接地址、方法出口等信息。每一个方法从调用直至执行完成的过程，就对应着一个栈桢在虚拟机中入栈到出栈的过程。

- 本地方法栈

  本地方法栈和虚拟机栈所发挥的作用是非常相似的，它们之间的区别不过是虚拟机栈为虚拟机执行 Java 方法服务，而本地方法栈则为虚拟机执行 Native 方法服务。

- 堆

  Java 堆是虚拟机管理的内存中最大的一块，此内存的唯一目的就是存放对象实例，几乎所有的对象实例都在这里分配内存。

- 方法区

  用于存储已经被虚拟机加载的类信息、常量、静态变量、即时编译器编译后的代码等数据。相对而言，垃圾回收在这个区域是比较少出现的。

**更多请参考：**

[Java 内存模型](https://www.jianshu.com/p/13b56ddad197)

[Java 内存区域](https://www.jianshu.com/p/2f0742032ab3)

### <span id="java_jvm_2">2. 简述垃圾回收器的工作原理？</span>
[https://www.jianshu.com/p/a238c56fd017](https://www.jianshu.com/p/a238c56fd017)
### <span id="java_jvm_3">3. 如何判断对象的生死？垃圾回收算法？新生代，老生代？</span>
### <span id="java_jvm_4">4. 哪些情况下的对象会被垃圾回收机制处理掉？</span>
### <span id="java_jvm_5">5. 垃圾回收机制与调用 System.gc() 的区别？</span>
### <span id="java_jvm_6">6. 强引用、软引用、弱引用、虚引用之间的区别？</span>

强引用：不会被 GC 轻易清理，只要引用存在，垃圾回收器永远不会回收。
```Java
Object obj = new Object();
```

软引用： 非必须引用，内存溢出之前进行回收
```Java
Object obj = new Object();
SoftReference<Object> sf = new SoftReference<Object>(obj);
obj = null;
sf.get();//有时候会返回 null
```

弱引用： 第二次垃圾回收时回收
```Java 
Object obj = new Object(); 
WeakReference wf = new WeakReference(obj); 
obj = null; wf.get();//有时候会返回 null 
wf.isEnQueued();//返回是否被垃圾回收器标记为即将回收的垃圾
```

虚引用： 垃圾回收时回收，无法通过引用取到对象值
```Java
Object obj = new Object();
PhantomReference<Object> pf = new PhantomReference<Object>(obj);
obj=null;
pf.get();//永远返回 null
pf.isEnQueued();//返回是否从内存中已经删除
```

### <span id="java_jvm_7">7. 强引用设置为 null，会不会被回收？</span>
### <span id="java_jvm_8">8. 简述 ClassLoader 类加载机制？</span>
### <span id="java_jvm_9">9. 对双亲委派模型的了解？</span>
### <span id="java_jvm_10">10. String a = "a"+"b"+"c" 在内存中创建几个对象？</span>

这个问题涉及到了字符串常量池和字符串拼接
```Java
String a = "a"+"b"+"c"
```

通过编译器优化后，得到的效果是
```Java
String a = "abc"
```

此时，如果字符串常量池中存在 abc，则该语句并不会创建对象，只是将字符串常量池中的引用返回而已。

如果字符串常量池中不存在 abc，则会创建并放入字符串常量池，并返回引用，此时会有一个对象进行创建。

两个深入阅读的链接：

- [字符串常量池](http://droidyue.com/blog/2014/12/21/string-literal-pool-in-java )
- [字符串拼接内部实现](http://droidyue.com/blog/2014/08/30/java-details-string-concatenation)

### <span id="java_jvm_11">11. 对 Dalvik、ART 虚拟机的了解？</span>
### <span id="java_jvm_12">12. 对动态加载（OSGI）的了解？</span>
### <span id="java_jvm_13">13. 常见编码方式有哪些？</span>
### <span id="java_jvm_14">14. utf-8 编码中的中文占几个字节？int 型占几个字节？</span>

## 其他

### <span id="java_other_1">1. 谈谈你对 Java 平台的理解？</span>
### <span id="java_other_2">2. Exception 和 Error 有什么区别？</span>
### <span id="java_other_3">3. 谈谈 final、finally、finalize 有什么不同？</span>
### <span id="java_other_4">4. 强引用、软引用、弱引用、幻想引用有什么区别？</span>
### <span id="java_other_5">5. String、StringBuffer、StringBuilder 有什么区别？</span>
### <span id="java_other_6">6. 动态代理基于什么原理？</span>
### <span id="java_other_7">7. int 和 Integer 有什么区别？</span>
### <span id="java_other_8">8. 对比 Vector、ArrayList、LinkedList 有何区别？</span>
### <span id="java_other_9">9. 对比Hashtable、HashMap、TreeMap 有什么不同？</span>
### <span id="java_other_10">10. 如何保证集合是线程安全的？ConcurrentHashMap 如何实现高效地线程安全？</span>
### <span id="java_other_11">11. Java 提供了哪些 IO 方式？NIO 如何实现多路复用？</span>
### <span id="java_other_12">12. Java 有几种文件拷贝方式？哪一种最高效？</span>
### <span id="java_other_13">13. 谈谈接口和抽象类有什么区别？</span>
### <span id="java_other_14">14. 谈谈你知道的设计模式？</span>
### <span id="java_other_15">15. synchronized 和 ReentrantLock 有什么区别？</span>
### <span id="java_other_16">16. synchronized 底层如何实现？什么是锁的升级、降级？</span>
### <span id="java_other_17">17. 一个线程两次调用 start() 方法会出现什么情况？</span>
### <span id="java_other_18">18. 什么情况下 Java 程序会产生死锁？如何定位、修复？</span>
### <span id="java_other_19">19. Java 并发包提供了哪些并发工具类？</span>
### <span id="java_other_20">20. 并发包中 ConcurrentLinkedQueue 和 LinkedBlockingQueue 有什么区别？</span>
### <span id="java_other_21">21. Java 并发库提供的线程池有哪几种？分别有什么特点？</span>
### <span id="java_other_22">22. AtomicInteger 底层实现原理是什么？如何在自己的产品代码中应用 CAS 操作？</span>
### <span id="java_other_23">23. 请介绍类加载过程，什么是双亲委派模型？</span>
### <span id="java_other_24">24. 有哪些方法可以在运行时动态生成一个 Java 类？</span>
### <span id="java_other_25">25. 谈谈 JVM 内存区域的划分，哪些区域可能发生 OutOfMemoryError？</span>
### <span id="java_other_26">26. 如何监控和诊断  JVM 堆内和堆外内存使用？</span>
### <span id="java_other_27">27. Java 常见的垃圾收集器有哪些？</span>
### <span id="java_other_28">28. 谈谈你的 GC 调优思路？</span>
### <span id="java_other_29">29. Java 内存模型中的 happen-before 是什么？</span>
### <span id="java_other_30">30. Java 程序运行在 Docker 等容器环境有哪些新问题？</span>
### <span id="java_other_31">31. 你了解 Java 应用开发中的注入攻击吗？</span>
### <span id="java_other_32">32. 如何写出安全的 Java 代码？</span>
### <span id="java_other_33">33. 后台服务出现明显“变慢”，谈谈你的诊断思路？</span>
### <span id="java_other_34">34. 有人说“Lambda 能让 Java 程序慢 30 倍”，你怎么看？</span>
[https://zhuanlan.zhihu.com/p/142271934](https://zhuanlan.zhihu.com/p/142271934)
### <span id="java_other_35">35. JVM 优化 Java 代码时都做了什么？</span>
### <span id="java_other_36">36. 谈谈 MySQL 支持的事务隔离级别，以及悲观锁和乐观锁的原理和应用场景？</span>
