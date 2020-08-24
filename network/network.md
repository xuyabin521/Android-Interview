# 网络基础

### <span id="quest_network_technological_process_1">1. 描述一次网络请求的流程?</span>
  1. 首先会通过 DNS 解析域名得到 IP 地址。
  2. 发送 HTTP 请求与头信息发送（HTTP 生成请求报文，TCP 把 HTTP 的报文按序号分割为多个报文段，进行3次握手）。
  3. 服务器进行应答，返回响应头内容和所需内容。
  4. 关闭 TCP 连接（4次挥手），看情况，还需要连接的话可以保持连接。

### <span id="quest_network_technological_process_2">2. TCP 中 3 次握手和 4 次挥手的过程?
三次握手过程   
第一次握手：A的TCP客户端进程也是首先创建传输控制块TCB，A将标志位SYN置为1，随机产生一个值seq=x，然后向B发出连接请求报文段（首部的同步位SYN=1，初始序号seq=x），SYN=1的报文段不能携带数据，但要消耗掉一个序号，此时TCP客户进程进入SYN-SENT（同步已发送）状态。   
第二次握手：服务端B收到连接请求报文段后，由标志位SYN=1得知Client请求建立连接，Server将标志位SYN和ACK都置为1，确认号ack=x+1，随机产生一个值作为初始序号seq=y，如同意建立连接，则向A发送确认报文段（SYN=1，ACK=1，ack=x+1，seq=y）确认连接，操作系统为该TCP连接分配TCP缓存和变量，此时TCP服务器进程进入SYN-RCVD（同步收到）状态。  
第三次握手：客户端A收到服务端B的确认后，检查ack是否为x+1，ACK是否为1，如果正确则将标志位ACK置为1，确认号ack置为y+1，序号seq置为x+1，并且此时操作系统为该TCP连接分配TCP缓存和变量，要向B给出确认报文段（ACK=1，ack=y+1，seq=x+1）。TCP连接已经建立，A进入ESTABLISHED（已建立连接）。当B收到A的确认后，也进入ESTABLISHED状态。

四次挥手  
第一次挥手：客户端A的应用进程先向服务端TCP发出连接释放报文段（FIN=1，序号seq=u），并停止再发送数据，主动关闭TCP连接，进入FIN-WAIT-1（终止等待1）状态，等待服务端B的确认。   
第二次挥手：服务端B收到连接释放报文段后即发出确认报文段（ACK=1，确认号ack=u+1，序号seq=v），服务端B进入CLOSE-WAIT（关闭等待）状态，此时的TCP处于半关闭状态。A收到B的确认后，进入FIN-WAIT-2（终止等待2）状态，等待B发出的连接释放报文段。   
第三次挥手：服务端B没有要向客户端A发出的数据，B发出连接释放报文段 （FIN=1，ACK=1，序号seq=w，确认号ack=u+1），B进入LAST-ACK（最后确认）状态，等待A的确认。   
第四次挥手：客户端A收到服务端B的连接释放报文段后，对此发出确认报文段（ACK=1，seq=u+1，ack=w+1），A进入TIME-WAIT（时间等待）状态。此时TCP未释放掉，需要经过时间等待计时器设置的时间2MSL后，A才进入CLOSED状态。
[https://www.jianshu.com/p/6b2e35fdaf2c](https://www.jianshu.com/p/6b2e35fdaf2c)
### <span id="quest_network_technological_process_3">3. TCP 与 UDP 的区别及应用?
首先TCP是面向连接的，UDP是无需连接的，TCP有着三握四挥，并且三次握手和四次挥手是对TCP建立的连接有着重要意义的两步，并且TCP是对IP无可靠性提供可靠性的源头，UDP继承了IP的特性，不保证不丢失包，不保证按顺序到达

TCP面向字节流，发送的时候是一个流，没有头尾，IP包不是一个流，而是一个个的IP包，UDP也是如此

TCP是有拥塞控制的，但是UDP没有

[https://www.jianshu.com/p/d23c0d4eba12](https://www.jianshu.com/p/d23c0d4eba12)
### <span id="quest_network_technological_process_4">4. HTTP 协议
[https://www.jianshu.com/p/7c8b4576e4bb](https://www.jianshu.com/p/7c8b4576e4bb)
### <span id="quest_network_technological_process_5">5. HTTP 1.0 与 2.0 的区别
[https://www.jianshu.com/p/be29d679cbff](https://www.jianshu.com/p/be29d679cbff)
### <span id="quest_network_technological_process_6">6. HTTP 报文结构
一个HTTP请求报文由四个部分组成：请求行、请求头部、空行、请求数据。  
[https://www.jianshu.com/p/e29a327f9441](https://www.jianshu.com/p/e29a327f9441)
### <span id="quest_network_technological_process_7">7. HTTP 与 HTTPS 的区别以及如何实现安全性
1.Url开头：HTTP 的 URL 以 HTTP:// 开头，而 HTTPS 的 URL 以 HTTPs:// 开头；  
2.安全性：HTTP 是不安全的，而 HTTPS 是安全的。HTTP协议运行在TCP之上，所有传输的内容都是明文，HTTPS运行在SSL/TLS之上，SSL/TLS运行在TCP之上，所有传输的内容都经过加密的。  
3.传输效率：传输效率上 HTTP 要高于 HTTPS ，因为 HTTPS 需要经过加密过程，过程相比于 HTTP 要繁琐一点，效率上低一些也很正常；  
4.费用：HTTP 无需证书，而 HTTPS 必需要认证证书；相比于 HTTP 不需要证书来说，使用 HTTPS 需要证书，申请证书是要费用的，HTTPS 这笔费用是无法避免的  
5.端口：HTTP和HTTPS使用的是完全不同的连接方式，用的端口也不一样，前者是80，后者是443。  
6.防劫持性：HTTPS可以有效的防止运营商劫持，解决了防劫持的一个大问题。
[https://blog.csdn.net/github_37130188/article/details/89463101](https://blog.csdn.net/github_37130188/article/details/89463101)
### <span id="quest_network_technological_process_8">8. HTTPS 原理
[https://zhuanlan.zhihu.com/p/27395037](https://zhuanlan.zhihu.com/p/27395037)
### <span id="quest_network_technological_process_9">9. 谈谈你对 WebSocket 的理解
[https://www.jianshu.com/p/c08cc2b21496](https://www.jianshu.com/p/c08cc2b21496)
### <span id="quest_network_technological_process_10">10. WebSocket 与 socket 的区别
[https://www.jianshu.com/p/c08cc2b21496](https://www.jianshu.com/p/c08cc2b21496)
### <span id="quest_network_technological_process_11">11. 视频加密传输


