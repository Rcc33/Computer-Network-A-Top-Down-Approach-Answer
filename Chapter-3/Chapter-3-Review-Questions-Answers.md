* **R1**  
a.  
运输层报文只需要包含目的端口号与数据部分。端口4字节，数据1196字节。  
b.  
运输层报文需要包含源端口号，目的端口号与数据部分。源端口号4字节，目的端口号4字节，数据1192字节。  
c.  
运输层在网络核心中不需要做任何事。  

* **R2**  
a.  
可以使用R1b的协议，写信的家庭成员是应用层，把信交给收集信件的家庭成员，代表运输层。运输层在信封上加上发信人的姓名和收件人的姓名，表示端口号，再把信交给邮政服务。  
b.  
不需要打开信封检信件内容。  

* **R3**  
源端口号y，目的端口号x  

* **R4**  
1. 允许少部分报文丢失
2. 要求一定发送速率，不想被TCP的拥塞控制所束缚

* **R5**  
可能是因为TCP有完善的丢失/差错时的重传机制，不需要再用户层处理数据丢失。

* **R6**  
可以得到可靠数据传输，在应用层检查数据是否完整，如果不完整则由应用层发送报文指示发送端重传。  

* **R7**  
两台报文段被描述为相同的套接字。  
应用层进程可以解析报文数据，也可以通过取得源主机的IP和端口号来识别两个不同主机。  

* **R8**  
通过不同的套接字传递。套接字都具有端口80。Web服务使用TCP，TCP的套接字是由源IP和端口号，目的IP和端口号共同确定的。

* **R9**  
需要确认收到的报文是新的报文还是对上一次报文的重传。  

* **R10**  
需要确认发送的报文是否丢失。  

* **R11**  
依然需要定时器来控制重传。

* **R12**  
没有Access Code，无法完成  

* **R13**  
没有Access Code，无法完成  

* **R14**  
a. 错  
b. 错  
c. 对  
d. 错  
e. 对  
f. 错  
假设旧SampleRTT都为0.9，则旧EstimatedRTT为0.9，DevRTT为0。  
新的SampleRTT为1，新的EstimatedRTT为0.9125，新的DevRTT为0.025。
则新的TimeoutInterval为0.9225，小于1  
g. 错  
同一报文中的确认号与该报文的初始序号和字节数无关  

* **R15**  
a. 20字节数据  
b. 确认号为90  

* **R16**  
用户键入R后，又发送了3个报文段  
A发送： Seq=43, ACK=80, data='R'  
B发送： Seq=80, ACK=44, data='R'  
A发送： Seq=44, ACK=81  

* **R17**  
两个都是R/2左右的速率  

* **R18**  
错，设为当前拥塞窗口值的一半  

* **R19**  
4*RTT<sub>FE</sub>是客户与前端服务器连接通信所需的时间。
在前端服务器收到请求时，会与远端服务器通信，由于TCP连接是持续的，没有建立连接的时间，因此所花时间为RTT<sub>BE</sub>。
再加上中间服务器处理的事件。  
