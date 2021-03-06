OSI参考模型的各层传输的数据和控制信息具有多种格式，常用的信息格式包括帧、数据包、数据报、段、消息、元素和数据单元。

 

信息交换发生在对等OSI层之间，在源端机中每一层把控制信息附加到数据中，而目的机器的每一层则对接收到的信息进行分析，并从数据中移去控制信息，下面是各信息单元的说明：

数据帧（Frame）：是一种信息单位，它的起始点和目的点都是数据链路层。

数据包（Packet）：也是一种信息单位，它的起始和目的地是网络层。

数据报（Datagram）：通常是指起始点和目的地都使用无连接网络服务的的网络层的信息单元。

段（Segment）：通常是指起始点和目的地都是传输层的信息单元。

消息（message）：是指起始点和目的地都在网络层以上（经常在应用层）的信息单元。

元素（cell）是一种固定长度的信息，它的起始点和目的地都是数据链路层。

元素通常用于异步传输模式（ATM）和交换多兆位数据服务（SMDS）网络等交换环境。

数据单元（data unit）指许多信息单元。常用的数据单元有服务数据单元（SDU）、协议数据单元（PDU）。

SDU是在同一机器上的两层之间传送信息。PDU是发送机器上每层的信息发送到接收机器上的相应层（同等层间交流用的）。

Packet（数据包）：封装的基本单元，它穿越网络层和数据链路层的分解面。通常一个Packet映射成一个Frame，但也有例外：即当数据链路层执行拆分或将几个Packet合成一个Frame的时候。

数据链路层的PDU叫做Frame（帧）；

网络层的PDU叫做Packet（数据包）；

TCP的叫做Segment（数据段）；

UDP的叫做Datagram。（数据报）——在网络层中的传输单元（例如IP）。一个Datagram可能被封装成一个或几个Packets，在数据链路层中传输

 

帧和数据包都是数据的传输形式。

帧，工作在二层，数据链路层传输的是数据帧，包含数据包，并且增加相应MAC地址与二层信息；

数据包，工作在三层，网络层传输的是数据包，包含数据报文，并且增加传输使用的IP地址等三层信息。 