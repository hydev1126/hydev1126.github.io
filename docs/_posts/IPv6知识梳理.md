---
title: IPv6知识梳理
published: 2025-03-14
date: 2025-03-14T15:34:00
tags:
  - IPv6
  - 网络数通
---
# IPv6介绍

## 什么是IPv6

网际协议第6版（英语：Internet Protocol version 6，缩写：IPv6）是网际协议的最新版本，用作互联网的协议。用它来取代IPv4主要是为了解决IPv4地址枯竭问题，同时它也在其他方面对于IPv4有许多改进。  
IPv6的设计目的是取代IPv4，然而长期以来IPv4在互联网流量中仍占据主要地位，IPv6的使用增长缓慢。在2022年4月，通过IPv6使用Google服务的用户百分率首次超过40%。  

## 背景与历史

现今的互联网络发展蓬勃，截至2018年1月，全球上网人数已达40.21亿，IPv4仅能提供约42.9亿个IP位置。虽然目前的网络地址转换及无类别域间路由等技术可延缓网络位置匮乏之现象，但为求解决根本问题，从1990年开始，互联网工程工作小组开始规划IPv4的下一代协议，除要解决即将遇到的IP地址短缺问题外，还要发展更多的扩展，为此IETF小组创建IPng，以让后续工作顺利进行。1994年，各IPng领域的代表们于多伦多举办的IETF会议中，正式提议IPv6发展计划，该提议直到同年的11月17日才被认可，并于1996年8月10日成为IETF的草案标准，最终IPv6在1998年12月由互联网工程工作小组以互联网标准规范（RFC 2460）的方式正式公布。

IETF曾提出过IPv6、IPv7、IPv8、IPv9等四个草案，并希望其中的一种协议能够替代IPv4。经过充分的讨论，IETF最终选择IPv6并替代IPv4，而IPv7、IPv8、IPv9也就从此销声匿迹。至于IPv5，1990年，IETF曾经提出过IPv5的草案，最初希望IPv5负责承载语音、视频等“流”业务，与负责承载数据业务的IPv4共同在网络运行。但这一草案仅停留在了时延阶段，没有被最终采用。

IP（Internet Protocol）是TCP/IP协议族中的网络层协议（网络层协议主要作用是：在互联网中进行寻址，引导数据包能够正确的到达目的地）。IPv4协议是目前广泛部署的因特网协议。在Internet发展初期，IPv4以其协议简单、易于实现、互操作性好的优势而得到快速发展。但随着网络的迅猛发展，IPv4协议的各种问题开始显现：

### 1、公有IP地址数量不足

IPv4地址由全球5个互联网地址分配机构管理负责，IPv4地址空间约42.9亿，实际可用约36.47亿个，已在2019年全部分配完毕，这意味着没有更多的IPv4地址可以分配给网络服务提供商或企业。作为严重稀缺资源，用户申请固定公有IP地址困难加大，并且费用十分昂贵。

### 2、设备维护的路由表表现数量过大

由于IPv4发展初期的分配规划问题，造成许多IPv4地址的分配不连续，不能有效聚合路由。日益庞大的路由表耗用大量内存，对设备成本和转发效率产生影响。

### 3、私有地址效率低

在IPv4地址枯竭阶段和IPv6过渡工作未完成之前，通过NAT技术暂时解决了地址匮乏和爆炸式增长的入网需求问题，但NAT技术本身也存在不足，例如，增加了网络的复杂度。由于维护IP地址间及端口号映射关系而增加的网络设备工作负担，使网络整体结构变得脆弱。互联网的本质是提供人与人之间的连接，NAT破坏了这个原则。

### 4、安全溯源难

IPv4制定时并没有仔细针对安全性进行设计，因此，固有的框架结构并不能支持端到端的安全。企业正在使用的IPv4网络，由于其在设计时几乎没有安全性考虑，随着地址枯竭和分配严重不平衡，NAT方式成为主流选择，即NAT背后的终端用户分配到的一般都是私有地址，网络中一旦有非法信息发布或者病毒传播，是难以追溯到源地址的，这大大加剧了网络安全问题。

## ICANN (IANA)和RIR

IANA 职能包括：协议参数管理、互联网号码资源管理以及域名管理。互联网名称与数字地址分配机构 (ICANN) 代表全球互联网社群履行上述职能。

### 协议分配

“协议参数管理”包括：维护互联网协议中使用的多个代码和编号。这项职能是在互联网工程任务组 (IETF) 的协同配合下完成的。

### 互联网号码资源

“互联网号码资源管理”包括：在全球范围内协调互联网协议编址系统（通常称为 IP 地址）。另外，此项职能还涉及将诸多自治系统编号 (ASN) 块分配给地区互联网注册管理机构 (RIR)。

### 根区管理

“根区管理”包括：分配顶级域（例如 .uk 和 .com）运营商，并维护其技术和管理信息。根区包含所有顶级域 (TLD) 的授权记录。

### IANA的发展史

IANA 职能是在管理 ARPANET（美国政府资助的国防部网络）期间制定的。最初只有 Jon Postel 一人来履行这些职能。从那以后，互联网有了极大的发展，IANA 职能现在由 ICANN 负责管理。

## 区域互联网注册管理机构 (RIR)

全球主要有五个区域互联网注册管理机构 (Regional Internet Registry，RIR)，它们负责各自区域内的 IP 地址分配、域名系统管理等工作。

- **APNIC (亚太网络信息中心)**：负责亚太地区的 IP 地址分配，包括中国、日本、韩国、澳大利亚等。
- **ARIN (美国网络信息中心)**：负责北美地区的 IP 地址分配，包括美国、加拿大等。
- **LACNIC (拉丁美洲和加勒比海网络信息中心)**：负责拉丁美洲和加勒比海地区的 IP 地址分配。
- **RIPE NCC (欧洲网络协调中心)**：负责欧洲地区的 IP 地址分配。
- **AFRINIC (非洲网络信息中心)**：负责非洲地区的 IP 地址分配。

![[RIR.png]]

![[IANA.png]]

## 中国互联网络信息中心 (CNNIC)

中国互联网络信息中心（China Internet Network Information Center，简称CNNIC）于1997年6月3日组建，是工业和信息化部直属科研事业单位，行使国家互联网络信息中心职能。

CNNIC是APNIC认定的中国大陆地区唯一的国家互联网注册机构(NIR)，于1997年成立了以CNNIC为召集单位的CNNIC IP地址分配联盟，帮助中国大陆地区的相关单位和组织从亚太互联网注册机构(APNIC )申请IP地址、AS号码互联网资源。  
中国的ISP/IDC/ICP/企事业单位，获得IP地址和AS号码最有效的方法是申请加入CNNIC分配联盟，向CNNIC申请IP地址和和AS号码资源。  

中国国家顶级域名包括“.CN”和“.中国”域名。中国互联网络信息中心（CNNIC）是我国国家顶级域名的注册管理机构。“.CN”域名是以CN为后缀的国家和地区代码顶级域名(ccTLD)，CN在全球互联网上代表中国。“.中国/.中國”域名是以“中国/中國”为后缀的域名，是全球互联网上代表中国的纯中文顶级域名，符合中文使用习惯。

新通用顶级域名".公司"、".网络"由中国互联网络信息中心负责运行和管理，同国家顶级域名一样，".公司"、".网络"域名由全国三大数据服务中心、覆盖全球的服务节点及监测节点所组成的全球服务平台提供运维与保障。".公司"、".网络"域名在互联网上表达着中国文化的传承，是企业品牌在互联网上的延伸，既满足用户中文上网的需要，又便于记忆及传播。

## IPv6地址编码

IPv6具有比IPv4大得多的编码地址空间。这是因为IPv6采用128位的地址，而IPv4使用的是32位。因此新增的地址空间支持2^128（约3.4×10^38）个地址，具体数量为340,282,366,920,938,463,463,374,607,431,768,211,456 个，也可以说成16^32个，因为每4位地址（128位分为32段，每段4位）可以取24=16个不同的值。

网络地址转换是目前减缓IPv4地址耗尽最有效的方式，而IPv6的地址消除了对它的依赖，被认为足够在可以预测的未来使用。就以地球人口70亿人计算，每人平均可分得约4.86×10^28（486117667×10^20）个IPv6地址。

从IPv4到IPv6最显著的变化就是网络地址的长度。RFC 2373和RFC 2374定义的IPv6地址有128位长；IPv6地址的表达形式一般采用32个十六进制数。

在很多场合，IPv6地址由两个逻辑部分组成：一个64位的网络前缀和一个64位的主机地址，主机地址通常根据物理地址自动生成，叫做EUI-64（或者64-位扩展唯一标识）。

# IPv6地址格式

IPv6二进位制下为128位长度，以16位为一组，每组以冒号“:”隔开，可以分为8组，每组以4位十六进制方式表示。例如：2001:0db8:86a3:08d3:1319:8a2e:0370:7344 是一个合法的IPv6地址。类似于IPv4的点分十进制，同样也存在点分十六进制的写法，将8组16位十六进制地址的冒号去除后，每位以点号“.”分组，例如：2001:0db8:85a3:08d3:1319:8a2e:0370:7344则记为2.0.0.1.0.d.b.8.8.5.a.3.0.8.d.3.1.3.1.9.8.a.2.e.0.3.7.0.7.3.4.4，其倒序写法用于ip6.arpa子域名记录IPv6地址与域名的映射。

同时IPv6在某些条件下可以省略：

1. 每项数字前导的0可以省略，省略后前导数字仍是0则继续，例如下组IPv6是等价的。
    
    2001:**0**db8:**0**2de:**0000**:**0000**:**0000**:**0000**:**0**e13
    
    2001:db8:2de:**0000**:**0000**:**0000**:**0000**:e13
    
    2001:db8:2de:**000**:**000**:**000**:**000**:e13
    
    2001:db8:2de:**00**:**00**:**00**:**00**:e13
    
    2001:db8:2de:**0**:**0**:**0**:**0**:e13
    
2. 可以用双冒号“::”表示一组0或多组连续的0，但只能出现一次：
    1. 如果四组数字都是零，可以被省略。遵照以上省略规则，下面这两组IPv6都是相等的。
        
        - 2001:db8:2de:**0**:**0**:**0**:**0**:e13
        
        2001:db8:2de**::**e13
        
        - 2001:0db8:0000:0000:0000:0000:1428:57ab
        
        2001:0db8:0000:0000:0000::1428:57ab
        
        2001:0db8:0:0:0:0:1428:57ab
        
        2001:0db8:0::0:1428:57ab
        
        2001:0db8::1428:57ab
        
    2. 2001**::**25de**::**cade 是非法的，因为双冒号出现了两次。它有可能是下种情形之一，造成无法推断。
        - 2001:0000:0000:0000:0000:25de:0000:cade
        - 2001:0000:0000:0000:25de:0000:0000:cade
        - 2001:0000:0000:25de:0000:0000:0000:cade
        - 2001:0000:25de:0000:0000:0000:0000:cade
    3. 如果这个地址实际上是IPv4的地址，后32位可以用10进制数表示；因此::ffff:192.168.89.9 相等于::ffff:c0a8:5909。

另外，::ffff:1.2.3.4 格式叫做**IPv4映射地址**。

IPv4位址可以很容易的转化为IPv6格式。举例来说，如果IPv4的一个地址为135.75.43.52（十六进制为0x874B2B34），它可以被转化为0000:0000:0000:0000:0000:FFFF:874B:2B34 或者::FFFF:874B:2B34。同时，还可以使用混合符号（IPv4-compatible address），则地址可以为::ffff:135.75.43.52。

由于同一非全局地址可能在同一范围的多个区域中使用（例如，在两条独立的物理链路中使用链路本地地址 fe80::1），而且一个节点可能连接到同一范围的不同区域的接口（例如，一个路由器通常有多个接口连接到不同的链路）。IPv6新增了区域ID（Zone ID）加以区分，或称作用域ID（Scope ID）。作用域ID仅用于本地链接，使用百分号追加在地址后面。其内容特定于操作系统，例如Windows使用数字 fe80::2%3 ，Linux使用网卡名字 fe80::2%eth0 。[[7]](https://zh.wikipedia.org/wiki/IPv6\#cite_note-rfc4007-7) 在URI中使用时，百分号需要进行编码，例如 fe80::a%en1 应显示为 http://[fe80::a%25en1] 。

## IPv6包头
### IPv6标准包头
- Version: 4 bits，IP协议版本号=6
- Traffic Class: 8bits，指示IPv6数据流通信类别或优先级。功能类似于IPv4的服务类型（TOS）字段。
- Flow Label: 20bits，IPv6新增字段，标记需要IPv6路由器特殊处理的数据流。该字段用于某些对连接的服务质量有特殊要求的通信，诸如音频或视频等实时数据传输。在IPv6中，同一信源和信宿之间可以有多种不同的数据流，彼此之间以非“0”流标记区分。如果不要求路由器做特殊处理，则该字段值置为“0”。
- Payload Length: 16bits，负载长度包括扩展头和上层PDU，16位最多可表示65535字节负载长度。超过这一字节数的负载，该字段值置为“0”，使用扩展头逐个跳段（Hop-by-Hop）选项中的巨量负载（JumboPayload）选项。
- Next Header: 8bits，识别紧跟IPv6头后的包头类型，如扩展头（有的话）或某个传输层协议头（诸如TCP，UDP或着ICMPIPv6）。
- Hop Limit: 8bits，类似于IPv4的TTL（生命期）字段。与IPv4用时间来限定包的生命期不同，IPv6用包在路由器之间的转发次数来限定包的生命期。包每经过一次转发，该字段减1，减到0时就把这个包丢弃。
- Source Address: 128bits，源IPv6地址。
- Destination Address: 128bits，目标IPv6地址。

![[ipv6包头.png]]

### IPv6扩展包头
IPv6包头设计中对原IPv4包头所做的一项重要改进就是将所有可选字段移出IPv6包头，置于扩展头中。由于除Hop-by-Hop选项扩展头外，其他扩展头不受中转路由器检查或处理，这样就能提高路由器处理包含选项的IPv6分组的性能。

通常，一个典型的IPv6包，没有扩展头。仅当需要路由器或目的节点做某些特殊处理时，才由发送方添加一个或多个扩展头。与IPv4不同，IPv6扩展头长度任意，不受40字节限制，以便于日后扩充新增选项，这一特征加上选项的处理方式使得IPv6选项能得以真正的利用。但是为了提高处理选项头和传输层协议的性能，扩展头总是8字节长度的整数倍。

目前，RFC2460中定义了以下6个IPv6扩展头：Hop-by-Hop（逐个跳段）选项包头、目的地选项包头、路由包头、分段包头、认证包头和ESP协议包头：

- Hop-by-Hop Options
- Destination Options (with Routing Options)
- Routing Header
- Fragment Header
- Authentication Header
- Encapsulation Security Payload Header
- Destination Options
- Mobility Header

# IPv6地址分类
## 常规地址

![[ipv6地址类型.png]]

### 单播（unicast）地址

单播地址标示一个网络接口。协议会把送往地址的数据包送往给其接口。IPv6的单播地址可以有一个代表特殊地址名字的范畴，如链路本地地址（link local address）和唯一区域地址（ULA，unique local address）。单播地址包括可聚类的全球单播地址（GUA，Global Unicast Address）、链路本地地址等。

### 任播（anycast）地址

任播像是Unicast（单点传播）与Broadcast（多点广播）的综合。单点广播在来源和目的地间直接进行通信；多点广播存在于单一来源和多个目的地进行通信。  
而Anycast则在以上两者之间，它像多点广播（Broadcast）一样，会有一组接收节点的地址列表，但指定为Anycast的数据包，只会发送给距离最近或发送成本最低（根据路由表来判断）的其中一个接收地址，当该接收地址收到数据包并进行回应，且加入后续的传输。该接收列表的其他节点，会知道某个节点地址已经回应了，它们就不再加入后续的传输作业。  
以目前的应用为例，Anycast地址只能分配给中间设备（如路由器、三层交换机等），不能分配给终端设备（手机、电脑等），而且不能作为发送端的地址。  

### 多播（multicast）地址

多播地址也称组播地址。多播地址也被指定到一群不同的接口，送到多播地址的数据包会被发送到所有的地址。多播地址由皆为一的字节起始，亦即：它们的前置为FF00::/8。其第二个字节的最后四个比特用以标明"范畴"。  
一般有node-local(0x1)、link-local(0x2)、site-local(0x5)、organization-local(0x8)和global(0xE)。多播地址中的最低112位会组成多播组群标识符，不过因为传统方法是从MAC地址产生，故只有组群标识符中的最低32位有使用。定义过的组群标识符有用于所有节点的多播地址0x1和用于所有路由器的0x2。  
另一个多播组群的地址为"solicited-node多播地址"，是由前置FF02::1:FF00:0/104和剩余的组群标识符（最低24位）所组成。这些地址允许经由邻居发现协议（NDP，Neighbor Discovery Protocol）来解译链接层地址，因而不用干扰到在区网内的所有节点。  

IANA对于多播地址的分配情况可以参考以下链接：
[https://www.iana.org/assignments/ipv6-multicast-addresses/ipv6-multicast-addresses.xhtml](https://www.iana.org/assignments/ipv6-multicast-addresses/ipv6-multicast-addresses.xhtml)

## 特殊地址

IANA对于特殊地址的分配情况可以参考以下链接：
[https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xhtml](https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xhtml)

### 未指定地址

::/128－所有比特皆为零的地址称作未指定地址。这个地址不可指定给某个网络接口，并且只有在主机尚未知道其来源IP时，才会用于软件中。路由器不可转送包含未指定地址的数据包。

### 链路本地地址（Link-Local Address）

::1/128－是一种单播绕回地址。如果一个应用程序将数据包送到此地址，IPv6堆栈会转送这些数据包绕回到同样的虚拟接口（相当于IPv4中的127.0.0.1/8）。  
fe80::/10－这些链路本地地址指明，这些地址只在区域连线中是合法的，这有点类似于IPv4中的169.254.0.0/16。  

### 本地站点地址（Site-Local Address）

FEC0::/10—IPv6的私网地址，已弃用。
1995 年 12 月，IPv6 地址块 fec0::/10 被保留用于站点本地地址，这些地址可在“站点”内用于私有 IPv6 网络。然而，由于“ 站点 ”一词定义不充分，导致路由规则的管理出现混乱。
2004年9月的RFC 3879已经不建议在新建的IPv6网络中使用Site-local地址，但是现有的IPv6环境仍可继续使用。Site-local由Unique-local地址取代。
对于无法访问internet的本地网络，可以使用网点本地地址，这个相当于IPv4里面的Private IP私有地址（10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16）。它的前10个bit是1111111011，IPv6标识为FEC0::/10。（注/10表示前10个bit固定，即固定为1111111011）。值得注意的是，在2004年9月的RFC3879中，已经不建议在新建的IPv6网络中使用Site-local地址。放弃的理由是，由于其固有的二义性带来的单播网点本地地址的复杂性超过了它们可能带来的好处。它在RFC4193中被ULA（Unique-local地址）取代。

### 唯一区域地址（Unique Local Address）

fc00::/7－唯一区域地址（ULA，unique local address）只可用于本地通信，类似于IPv4的专用网络地址10.0.0.0/8、172.16.0.0/12和192.168.0.0/16。这定义在RFC 4193中，是用来取代站点本地位域。这地址包含一个40比特的伪随机数，以减少当网站合并或数据包误传到网络时碰撞的风险。这些地址除了只能用于区域外，还具备全局性的范畴，这点违反了唯一区域位域所取代的站点本地地址的定义。
FC00::/8 是被保留的，但这并不意味着它不可用，而是被保留为未来可能用途，尚未被标准完全定义。目前，实际使用的是 FD00::/8子集，这就是我们常说的 ULA 地址。

### 多播地址（Multicast Address）

ff00::/8－这个前置表明定义在"IP Version 6 Addressing Architecture"（RFC 4291）中的多播地址[12]。其中，有些地址已用于指定特殊协议，如ff0X::101对应所有区域的NTP服务器（RFC 2375）。

### 请求节点多播地址（Solicited-node multicast address）

ff02::1:FFXX:XXXX－XX:XXXX为相对应的单播或任播地址中的三个最低的字节。

### IPv4转译地址

::ffff:x.x.x.x/96－用于IPv4映射地址。（参见以下的转换机制）。  
2001::/32－用于Teredo隧道。  
2002::/16－用于6to4。  
### ORCHID

2001:10::/28－ORCHID (Overlay Routable Cryptographic Hash Identifiers)（RFC 4843）。这些是不可绕送的IPv6地址，用于加密散列识别。

### 文件

2001:db8::/32－这前置用于文件（RFC 3849）。这些地址应用于IPV6地址的示例中，或描述网络架构。

### 遭舍弃或删除的用法

::/96－这个前置曾用于IPv4兼容地址，现已删除。  
fec0::/10－这个站点本地前置指明这地址只在组织内合法。它已在2004年9月的RFC3879中舍弃，并且新系统不应该支持这类型的地址。  

# IPv6地址规划

  

# IPv6部署与应用

2017年11月26日中共中央办公厅、国务院办公厅印发了《推进互联网协议第六版（IPv6）规模部署行动计划》，明确了推进IPv6部署的重要意义，提出了部署的总体要求和主要目标，要用5到10年时间，形成下一代互联网自主技术体系和产业生态，建成全球最大规模的IPv6商业应用网络，实现下一代互联在经济社会各领域深度融合应用。为贯彻落实中共中央办公厅、国务院办公厅印发的《推进互联网协议第六版（IPv6）规模部署行动计划》，加快网络基础设施和应用基础设施升级步伐，促进下一代互联网与经济社会各领域的融合创新，工信部发布关于贯彻落实《推进互联网协议第六版(IPv6)规模部署行动计划》通知，积极推进内部网络和应用IPv6改造，加快推进企业生产管理信息系统等内部网络和应用的IPv6改造，加强IPv6环境下移动互联网、物联网、工业互联网、云计算、大数据、人工智能等研究与应用，强化IPv6环境下网络安全保障等。物联网、移动互联网、云计算等新兴产业的发展都需要海量的IP地址作为支撑，IP地址不足已经严重制约着这些处于全球竞争前沿、具有最广阔前景的新兴产业发展。随着物联网、移动互联网、云计算等业务不断发展壮大，运营商不停地扩大网络规模，这也使IPv4地址枯竭的速度更快了，分配殆尽的IPv4地址已经成为制约我国物联网、移动互联网、云计算发展的瓶颈。

2018年3月12日，国资委印发了《关于做好互联网协议第六版（IPv6）部署应用有关工作的通知》，要求央企在18年完成门户网站和面向用户的在线服务窗口的IPv6改造。2018年5月3日，工信部发布《推进互联网协议第六版(IPv6)规模部署行动计划》通知，鼓励典型行业、重点工业企业开展工业互联网IPv6网络化改造，创新工业互联网应用实践，构建工业互联网IPv6标准体系。为响应国家IPv6发展，企业开展基于IPv6的创新业务，对网络接入、内部网络及系统提出新的需求。企业IPv6升级解决方案根据企业内部现有网络及系统情况，提供从内部网络IPv6升级改造技术路线到企业系统的IPv6规划、升级和部署相关解决方案，以满足企业开展IPv6业务，适用于工业互联网网络体系中工厂控制系统和工业云平台部分。

2024年4月，中央网信办、国家发展改革委、工业和信息化部联合印发《深入推进IPv6规模部署和应用2024年工作安排》（以下简称《工作安排》）。

通知要求，坚持以习近平新时代中国特色社会主义思想为指导，全面贯彻落实党的二十大精神，完整、准确、全面贯彻新发展理念，以全面推进IPv6技术创新与融合应用为主线，着力破解瓶颈短板，完善技术产业生态，打造创新引领、高效协同的自驱性发展态势，为建设网络强国、数字中国提供有力支撑。

《工作安排》明确了2024年工作目标：到2024年末，IPv6活跃用户数达到8亿，物联网IPv6连接数达到6.5亿，固定网络IPv6流量占比达到23%，移动网络IPv6流量占比达到65%。IPv6网络性能显著提高，使用体验提升明显。云服务、内容分发网络、数据中心在业务开通时默认启用IPv6功能。主要商业网站及移动互联网应用IPv6支持率达到95%，IPv6行业融合应用更加深入广泛。固定网络IPv6贯通水平大幅跃升，新出厂家庭路由器、机顶盒等终端设备默认启用IPv6，存量家庭路由器IPv6开启率明显提升，企业机构互联网专线IPv6开通率明显提高。IPv6单栈支持能力持续增强。“IPv6+”创新技术应用领域进一步拓展。IPv6标准体系持续完善，立项IPv6国家标准达到50项。

《工作安排》部署了十个方面重点任务。

**一是增强IPv6网络性能和服务质量。**包括加大IPv6网络优化力度、优化IPv6业务开通流程、持续提升IPv6互联互通水平、持续深入推进广电网络IPv6改造。

**二是提高应用设施IPv6部署水平。**包括加强云产品IPv6推广应用、提升内容分发网络IPv6流量占比、强化数据中心承载业务IPv6升级改造、推动算力基础设施同步部署IPv6。

**三是提高终端设备IPv6连通水平。**包括提升家庭路由器IPv6使用水平、扩大家庭智能终端IPv6支持范围、加快推进物联网IPv6应用。

**四是强化先行先试和示范引领。**包括开展重点城市IPv6专项行动、强化试点示范作用、推动党政机关办公网络率先开通IPv6、强化推进IPv6规模部署和应用专家委平台作用。

**五是推进IPv6单栈部署演进。**包括增强IPv6单栈运行能力、拓展IPv6单栈试点部署范围。

**六是深化行业融合应用。**包括深化中央企业行业系统IPv6改造、提升金融机构IPv6创新应用水平、推进农业农村部系统IPv6升级改造、深化教育行业IPv6部署应用、推进各级人社部门IPv6部署应用、推进民政信息系统IPv6部署应用、加强医疗卫生机构IPv6升级改造、推进交通数字化设施IPv6应用、拓展工业互联网IPv6应用、深化水利行业IPv6部署应用、加大自然资源与生态环境信息化IPv6改造力度、推动应急管理业务系统和终端支持IPv6。

**七是扩大IPv6内容源规模。**包括深化政务网络和应用服务IPv6升级改造、拓展商业应用IPv6支持范围。

**八是推进创新生态和标准体系建设。**包括强化“IPv6+”创新产业生态建设、加强互联网体系结构创新研究、持续推进IPv6国家标准制定与实施、积极参与IPv6技术国际标准制定。

**九是强化网络安全保障。**包括加快IPv6安全技术产品研发应用、加强IPv6网络安全防护和管理监督。

**十是加大宣传推广力度。**包括创新宣传形式和内容、丰富行业交流活动。

## NAT64

随着互联网的发展，大量企业开始部署对公应用、暴露应用API，面对IPv6的改革需求，在应用还没有完全准备好之前，企业如何快速将应用通过IPv6暴露给互联网用户？

通过NAT64技术在互联网专线入口部署NAT64设备（如：防火墙、路由器、负载均衡设备等）进行IPv6到IPv4的地址映射，可以快速实现应用IPv6的发布。NAT64技术对于内部应用而言还是IPv4的环境，但对于终端用户而言，已经可以使用IPv6访问企业应用。

NAT64虽然可以快速实现IPv6的应用发布，但是也存在一些问题，如：

- 需要网络设备的功能支持
- NAT64带来的性能损耗
- 增加溯源难度

## IPv4&IPv6双栈部署

除了使用NAT64技术外，也可以使用双栈部署的模式，从底层基础设施到上层应用全面支持IPv6，包括：路由器、交换机、防火墙、虚拟化环境、操作系统、应用、中间件、数据库等。双栈部署的模式可以全面实现端到端IPv6的访问需求，减少NAT64带来的性能损耗，同时对于一些有溯源需求的应用场景更加友好。

## 基础架构对IPv6的支持

### 网络设备

无论是IPv4还是IPv6协议，网络设备都起着重要的传输作用，为了更好的支持IPv6协议，网络设备需要从软件支持性、硬件性能这2个方面重点考虑；

- 软硬件支持性：现网存在的大量设备可能都比较老旧，从软硬件上可能都不支持IPv6协议，有些设备即使可以通过升级最新软件来支持IPv6协议，但又可能因为硬件过于老旧无法升级到最新的软件版本；
- 设备性能：同样由于设备比较老旧，或者一些其它原因，设备对于IPv6的性能可能远不及IPv4下的场景；

### 操作系统

现代操作系统无论是Server端的Windows、Linux、IOS、Android等，大部分都能原生支持IPv6协议

- IPv4&IPv6双协议栈地址配置
- IPv6协议栈开关功能
    
    如果网关没有关闭SLAAC或启用了DHCPv6后，操作系统会自动配置IPv6地址，同时改变原本单IPv4协议栈下的一些行为，如：发起AAAA记录DNS的请求，获得对应的结果后，系统会优先通过IPv6地址发起访问，这时候如果网络还没完准备好可能会导致访问异常；在一个网络中如果存在一些主机不需要IPv6的场景，可以通过修改配置的方式手动关闭IPv6协议栈，避免系统自动配置IPv6地址。
    
- 手动配置IPv6地址
    
    对于Server端的主机最好使用手动配置IPv6地址的方式，在有策略控制的场景下可以做到精确控制，降低运维复杂度；
    
- 自动配置IPv6地址
    - DHCPv6
        
        对于终端主机可以通过DHCPv6服务提供IPv6地址自动获取的功能
        
    - SLAAC
        
        对于终端主机，通过EUI-64的方式实现IPv6地址自动配置
        

### EUI-64规则

IPv6中有一种成为无状态自动配置的机制使用EUI-64地址来自动配置IPv6地址，EUI-64格式即扩展唯一标识符，相当于MAC-48地址。所谓无状态自动配置是指在网络中没有DHCP服务器的情况下，允许节点自行配置IPv6地址的机制。

内嵌MAC地址又称为EUI-64地址，是通过设备MAC地址产生的，首先在48位的MAC地址的中间位置，插入十六进制数FFFE，并且要U/L（Universal/Local）位（从高位开始的第7位)取反，最后得到的就是64位EUI-64格式地址。这类地址的主要特征是地址中包含FFFE字符。

自动将48位的以太网MAC地址扩展为64位，再挂在一个64位的前缀后面，组成一个IPv6地址，步骤共有三步。

第一步，将48位的MAC地址从中间分开，插入一个固定的FFFE（16进制）

第二步，将第7位比特位反转，如果原来是0就变为1，如果原来是1就变为0.

第三步，加上64位的网络前缀这就是一个完整的IPv6地址。

在MAC地址中，第7比特位1表示本地管理，为0表示全球管理。

在EUI-64中，第7位为1表示全球唯一，为0表示本地地址。

- 转换示例如：
    - 原MAC48地址为39-A7-94-07-CB-D0，从中间断开插入FF-FE，变为39-A7-94--FF-FE-07-CB-D0。
    - 第7个比特反转（从左往右数），变为3B-A7-94-FF-FE-07-CB-D0
    - 加入网络前缀，若前缀为链路本地地址则网络前缀为FE-80-00-00-00-00。IPV6地址最终为FE-80-00-00-00-00-00-00-3B-A7-94-FF-FE-07-CB-D0。可简写为FE80::3BA7:94FF:FE07:CBD0

![[EUI-64转换方式.png]]
### DNS系统

DNS解析是互联网访问的第一步，无论是使用笔记本浏览器访问网络还是打开手机APP的时候，访问的第一步必然要经过DNS解析流程。对于一个比较复杂的网站来说，DNS解析时间大概占到初始页面登录时间的29%，所以整个DNS解析的性能对于访问一个网站有着至关重要的作用。如果DNS比较差，或者它的稳定性比较差，可能会对用户的访问带来非常大的影响。

DNS系统需要完成以下任务：

- 域名到IPv4&IPv6双栈的解析
- 流量精确调度
- 应用系统探测
- 单IP协议栈故障场景下的解析切换

### DNS解析记录

**一、A记录**

A（Address）记录是用来指定主机名（或域名）对应的IP地址记录。用户可以将该域名下的网站服务器指向到自己的web server上，同时也可以设置域名的子域名。简单来讲，A记录就是指定域名对应的IP地址。如我们添加一条A记录将www的主机指向IP192.168.1.1，那么当你访问www主机时就会解析到192.168.1.1这个IP上。

**二、CNAME记录**

通常称别名解析，是主机名到主机名的映射。当需要将域名指向另一个域名，再由另一个域名提供 IP 地址，就需要添加 CNAME 记录，最常用到 CNAME的场景包括做CDN、企业邮箱、全局流量管理等。与A记录不同的是，CNAME别名记录设置的值不是一个固定的IP，而是主机的别名地址。

别名解析可以提供更大的灵活性，便于统一管理。比如，当主机因某种因素的影响需要更换IP时，如果域名做了CNAME记录，就可以同时更新别名的解析指向，不需要进行新的解析操作。

**三、NS记录**

如果需要把子域名交给其他DNS服务商解析，就需要添加NS记录（Name Server）。NS记录是域名服务器记录，用来指定该域名由哪个DNS服务器来进行解析。NS记录中的IP即为该DNS服务器的IP地址。大多数域名注册商默认用自己的NS服务器来解析用户的DNS记录。DNS服务器NS记录地址一般以以下的形式出现：ns1.domain.com、ns2.domain.com等。

**四、SOA记录**

SOA，是起始授权机构记录，说明了在众多 NS 记录里哪一台才是主要的服务器。在任何DNS记录文件中，都是以SOA ( Startof Authority )记录开始。SOA资源记录表明此DNS名称服务器是该DNS域中数据信息的最佳来源。

SOA记录与NS记录的区别：NS记录表示域名服务器记录，用来指定该域名由哪个DNS服务器来进行解析；SOA记录设置一些数据版本和更新以及过期时间等信息。

**五、AAAA记录**

AAAA记录(AAAA record)是用来将域名解析到IPv6地址的DNS记录。用户可以将一个域名解析到IPv6地址上，也可以将子域名解析到IPv6地址上。国内大多数IDC不支持AAAA记录的解析，因此如果想进行AAAA记录解析，则需对域名NS记录设置一些专业的域名解析服务商，由他们提供AAAA记录的设置。国科云云解析支持IPv6环境下的AAAA记录解析。

**六、TXT记录**

TXT记录，一般指某个主机名或域名的标识和说明。如：admin IN TXT "管理员, 电话：XXXXXXXXXXX"，mail IN TXT "邮件主机，存放在xxx , 管理人：AAA"，Jim IN TXT "contact: abc@mailserver.com"，也就是说，通过设置TXT记录内容可以使别人更方便地联系到你。TXT 记录常用的方式还有做 SPF 记录（反垃圾邮件）和SSL证书的DNS验证等。

**七、MX记录**

MX（Mail Exchanger）记录是邮件交换记录，主要用于邮箱解析，在邮件系统发送邮件时根据收信人的地址后缀进行邮件服务器的定位。MX记录允许设置一个优先级，当多个邮件服务器可用时，会根据该值决定投递邮件的服务器。

MX记录的权重对 Mail 服务非常重要，当发送邮件时，Mail 服务器先对域名进行解析，查找 MX记录。先找权重数最小的服务器（比如说是 10），如果能连通，那么就将服务器发送过去；如果无法连通 MX 记录为 10 的服务器，才将邮件发送到权重更高的 mail 服务器上。

**八、PTR记录**

PTR是pointer 的简写，即“反向DNS”，domain name pointer，可以粗略的理解为DNS反向，是一个指针记录，用于将一个IP地址映射到对应的主机名，也可以看成是A记录的反向，即通过IP访问域名。

**九、SRV记录**

即服务定位（SRV）资源记录，用于定义提供特定服务的服务器的位置，如主机（hostname），端口（port number）等。

**十、URL转发**

URL转发，是指通过服务器的特殊设置，将当前访问的域名指向另一个指定的网络地址。根据目标地址的隐藏与否，URL转发可以分为显性URL和隐性URL两种。

**显性URL：**将域名指向一个http（s)协议地址，访问域名时，自动跳转至目标地址，地址栏显示为目标网站地址。

**隐性URL：**与显性URL类似，但隐性转发会隐藏真实的目标地址，地址栏中显示为仍为此前输入的地址。

### 应用系统

应用系统对于IPv6的支持主要由应用程序决定，如nginx、apache、redis、kafka、mysql、oracle等，对于应用组件对于IPv6的支持以及开启方法，建议查询各组件官网的支持文档；

## 终端对IPv6的支持

![[终端对IPv6支持情况.png]]

## Happy Eyeballs

Happy Eyeballs（快乐眼球），亦被称作 Fast Fallback（快速回退），是一个由 IETF 发布的算法。支持该算法的程序会尝试同时使用 IPv4 和 IPv6 协议进行连接，若两者皆可连通则首选 IPv6，使得同时支持 IPv4 和 IPv6 的双栈应用程序对用户的响应更加灵敏，从而最大限度地减少IPv6连接或设置不完善的用户遇到的常见问题。 “快乐眼球”一词源自行内术语“眼球”，用于描述互联网上那些面向人类用户（而不是服务器）的端点，因此“快乐眼球”此处用于形容快乐的用户。  
由于许多互联网用户尚无法访问 IPv6 互联网，当这些用户的应用程序尝试访问 IPv6 网络时，这些应用程序会进入无响应状态，从而影响用户体验。Happy Eyeballs 以并行的方式尝试使用两种协议发起连接，来判断使用哪种协议更为合适，而并行的运用意味着该判断过程的延迟和普通连接几乎一致，因而解决了这个问题。使用的地址通常是通过循环算法从 DNS 中选择的。  
谷歌的Chrome游览器、Opera游览器、Firefox、cURL、OSX、OpenBSD等软件皆实现了Happy Eyeballs算法。  
Happy Eyeballs 曾于2011年世界IPv6日进行了一次测试。  
Happy Eyeballs 算法也可以扩展到用于判断最佳的传输协议类型，如TCP和SCTP，但其开发仍处于实验阶段。  

# IPv6相比IPv4带来的变化

## ND vs ARP解析

[https://www.networkacademy.io/ccna/ipv6/neighbor-discovery-protocol](https://www.networkacademy.io/ccna/ipv6/neighbor-discovery-protocol)

IPv4 和 IPv6 之间的区别之一是不再使用 ARP（地址解析协议）。 ND（邻居发现协议）取代了 ARP 的功能。

ND使用ICMPv6和solicited-node multicast addresses来发现同一个网络上其它IPv6主机的二层地址，ND定义了5个类型的消息封装在ICMPv6协议中

- Router Solicitation (ICMPv6 type 133)
- Router Advertisement (ICMPv6 type 134)
- Neighbor Solicitation (ICMPv6 type 135)
- Neighbor Advertisement (ICMPv6 type 136)
- Redirect Message (ICMPv6 type 137)

### Neighbor Solicitation (NS)

When a node needs to resolve the physical address of a known IPv6 address, it sends a Neighbor Solicitation (NS) message on the network segment. This message is the IPv6 alternative to the ARP Request. There are few changes in comparing to ARP though that makes the Neighbour Solicitation **more secure and efficient**.

Let's look at the example shown in figure 1 where PC1 wants to resolve the physical address of PC3 - FE80::20C:CFF:FECC: CCCC.  PC1 needs to send a Neighbour Solicitation message for this IPv6 address so it creates a new ICMPv6 packet type 135. Type 135 explicitly tells the receiving side that this is an NS packet. In the target field of the ICMPv6, PC1 puts the IPv6 address that it wants to find the MAC of. In our example, it would be one of PC3 -  FE80::20C:CFF:FECC:CCCC.

This ICMPv6 message is then encapsulated in an IPv6 packet. For source address at layer 3, PC1 sets its own link-local address FE80:20A:AFF:FEAA:AAAA. The destination address is key in the improved security and efficiency comparing to the ARP protocol in IPv4. For destination address in the IPv6 packet, PC1 set a special type of multicast address called _**solicited-node**_ multicast.  For each configured IPv6 address, every node joins a multicast group identified by the address FF02::1:FFXX:XXXX where XX:XXXX are the last 6 hexadecimal values in the IPv6 unicast address. Therefore, for each configured unicast address, no matter if it is link-local or global, the host joins the respective auto-generated _**solicited-node**_ multicast group.

In our example, PC1 wants to send the NS message to the node with IP address FE80::20C:CFF:FECC: CCCC. Having the above logic in mind, the node that has that IPv6 address must have joint the solicited-node group generated from that address - FF02::1:FFCC:CCCC.
![[ipv6-neighbor-solicitation.png]]
_Figure 1. IPv6 Neighbor Solicitation Message_

After the IPv6 header is filled, the packet is encapsulated in an Ethernet frame. For source MAC address, PC1 sets its own burnt-in physical address. The destination MAC address is set to a multicast MAC generated from the multicast IPv6 address in the layer 3 header using the following formula. 3333.XXXX.XXXX where XXXX:XXXX are the last 8 hex digits in the multicast IPv6 address. In our example, this will result in the physical address of 3333.FFCC.CCCC because are the last 8 hex digits in the destination address FF02::1:FFCC:CCC.

When PC1 sends this Neighbor Solicitation message on the network, there are two possible scenarios:

- If switches in the local segment are running a protocol called IPv6 Multicast Listener Discovery Snooping (MLD), they will know that only PC3 is subscribed to the multicast group FF02::1:FFCC:CCC and will switch the frame only to PC3.
- If the switches in the local segment are not running MLD, they will broadcast the frame to every node in the segment in the same way as an ARP frame in IPv4. However, only PC3 will process the packet, because only PC3 is subscribed to this multicast group. All other nodes that get this NS packet will discard it, because they do not listen to this solicited-node address FF02::1:FFCC:CCC.

### Neighbor Advertisement (NA)

When PC3 gets the Neighbor Solicitation message from PC1, it will look at the Target field in the ICMPv6 header and will compare it against its own configured IPv6 addresses. The target address matches PC3's link-local address, so PC3 will reply back to PC1 with a message called Neighbor Advertisement. This message is the IPv6 alternative to the ARP Reply in IPv4.

Let's examine in detail all values in the message. In the ICMPv6 header, PC3 sets the Type field to 136, which means that this is a NA message. In the _Target_ field, P3 sets the IPv6 address and in the _Link-local Address_ field, it sets the physical address of the interface configured with this IPv6.

![[ipv6-neighbor-advertisement-message_0.png]]

_Figure 2. IPv6 Neighbor Advertisement Message_

In the IPv6 header, PC3 sets the source IPv6 address to be its link-local address and the destination to be the link-local address of PC1.

In the Ethernet header, PC3 sets its own physical address as source MAC and the physical address of PC3 as destination MAC. Note that the Neighbor Advertisement is **a unicast message**.

### **Router Advertisement (RA)**

IPv6 routers attached to a local segment advertise their presence periodically via an ICMPv6 message called **Router Advertisement (RA)**. The message is destined to the _**all-nodes**_ multicast address FF02::1 which means that every node on the segment receives and processes it. RA messages contain the _prefix_ and the _prefix length_ used on this segment as well as other parameters such as MTU. Cisco routers advertise their presence on a segment every 200 seconds by default.

![[ipv6-router-advertisement-message_0.png]]
_Figure 3. IPv6 Router Advertisement Message_

Nodes use these messages for services such as Stateless Autoconfiguring (SLAAC) which we explain in detail in [this lesson](https://www.networkacademy.io/ccna/ipv6/stateless-address-autoconfiguration-slaac).

### **Router Solicitation (RS)**

As we said above, Cisco routers send Router Advertisement messages every 200 seconds by default. However, when a node is connected to a local segment, it sends out a message called Neighbor Solicitation that requests that routers generate Router Advertisements (RA) immediately rather than at their next scheduled time.

![[ipv6-router-solicitation-message_0.png]]

_Figure 4. IPv6 Router Solicitation Message_

As you can see in the example in figure 4, the Router Solicitation message is destined to the _**all-routers**_ multicast address, which means that only the routers on the local segment will process these RS messages.

### **Summary**

IPv6 Neighbor Discovery Protocol works by using 5 types of messages encapsulated in ICMPv6. Each message has the following purpose:

- **Router Solicitation** - Hosts use Router Solicitation messages to locate routers in their local segment. Upon receipt of an RS message, routers generate Router Advertisements immediately rather than at their next scheduled time. The RS message uses ICMPv6 type 133 and is destined to the **all-routers** multicast address FF02::2.
- **Router Advertisement** - IPv6 routers advertise their presence in the local segments either periodically, or in response to a Router Solicitation. The RA message uses ICMPv6 type 134 and is destined to the **all-nodes** multicast address FF02::1. Cisco router sent RA messages every 200 seconds by default.
- **Neighbor Solicitation** - The Neighbor Solicitation message is used by nodes to resolve the physical address of a known IPv6 address (target address). The NS message is encapsulated in ICMPv6 type 135 and is destined to the **solicited-node multicast group** that is auto-generated from the targeted IPv6 address. Only the owner of the targeted IP must have subscribed to this solicited-node group. The message has a similar function to the IPv4 ARP Request but is **more secure and efficient** because it is not broadcasted to all nodes.
- **Neighbor Advertisement** - Neighbor advertisements are used by nodes to respond to a Neighbor Solicitation message. The NA message is encapsulated in ICMPv6 type 136 and is destined for the **unicast address** in the Neighbor Solicitation message.
- **Redirect Message** - Routers informs hosts of a better first-hop router for a destination.

## ICMPv6的应用

## Path MTU Discovery

在IPv4环境中，如果一个数据包的大小超过某台设备outgoing接口的MTU时，并且DF-bit (don't fragment)没有被置位的情况下，该设备会将原数据包拆分成符合MTU大小的多个数据包后再进行传输。

在IPv6环境中，路由器不进行分片操作，当路由器收到一个大于outgoing接口MTU的数据包时，会发送ICMPv6 “Packet Too Big”消息通知发送者，并且该消息中还会包含设备接口MTU的大小供发送者参考进行数据包分片，这个过程称作Path MTU Discovery。

### **Fragmentation in IPv4 and IPv6**

If you look closely at the IPv4 header fields, you will note three fields that are not present in the IPv6 Header - the _**Identification**_, _**Flags**_, and _**Fragmentation Offset**_ fields. They have been removed in version 6 because of the difference in the way fragmentation is handled in both protocols.

In IPv4, all network layer devices are allowed to fragment packets if the DF-bit (don't fragment) is not set. For example, if a router receives a packet that is larger than the MTU of the outgoing interface, the router divides the packet into multiple packets and send them out. The final destination is then responsible to reassemble the fragments into the original IP packet. Such an example is shown in figure 9.

![[ipv4-fragmentation-example.gif]]
_Figure 10. IPv4 Fragmentation is done by a router_

The three IPv4 fields _**Identification**_, _**Flags**_, and _**Fragmentation Offset**_ are used in this fragmentation handling process.

In IPv6, routers do not fragment packets. When an IPv6 router receives a packet larger than the MTU of the outgoing interface, the router discards the packet and sends an ICMPv6 "Packet Too Big" message back to the sender. The message includes the MTU value of the egress link, so the source can adjust the packet size and retransmit. This process is called Path MTU Discovery and is described in [RFC 1981](https://tools.ietf.org/html/rfc1981), _Path MTU Discovery for IP Version 6_. An example is shown in figure 10.

There are two important points to clarify:

- Typically, when a source starts sending packets to a destination, it is not a single packet but a series of multiple ones. This process of adjusting the MTU is happening only with the first packet and after that, the entire flow is being transmitted with the proper packet size.
- Obviously, IMCPv6 messages have to be able to reach the sender for PMTU to work. Oftentimes, ICMPv6 is filtered out on firewalls or other security devices, and the PMTU process breaks.

![[ipv6-fragmentation.gif]]

_Figure 11. IPv6 Fragmentation is done by the source_

## DHCP服务

在IPv6中可以通过以下三种方法自动配置或下发IP地址

- SLAAC
    
    基于前缀+EUI-64的方式自动生成IPv6地址，但是SLAAC只能生成地址却无法像DHCP一样提供DNS等其它服务；
    
- Stateless DHCPv6
    
    将SLAAC和DHCP服务结合，通过SLAAC生成IPv6地址，通过DHCP服务下发DNS和域名等信息；
    
- Stateful DHCPv6
    
    同时提供IPv6地址和DNS、域名等信息；DHCPv6和DHCPv4的一个重要区别是，DHCPv6不下发网关地址，网关地址由路由器的RA报文提供
    

## DNS解析

![[终端对IPv6支持情况.png]]

## 溯源问题

X-Forward-For：176.201.31.3

X-Forward-For：2002:2480:2392:AD22::1

部分应用系统需要通过该字段实现溯源需求

记录值会写入日志系统、审计系统、本地磁盘、存储、数据库

需确认先关组件是否对该字段值的长度有限制，如有长度限制将导致写入失败，严重时会影响正常业务

  

# 参考资料

- [https://www.icann.org/zh/system/files/files/iana-functions-18dec15-zh.pdf](https://www.icann.org/zh/system/files/files/iana-functions-18dec15-zh.pdf)
- [https://zh.wikipedia.org/wiki/IPv6](https://zh.wikipedia.org/wiki/IPv6)
- [https://info.support.huawei.com/info-finder/encyclopedia/zh/IPv6.html](https://info.support.huawei.com/info-finder/encyclopedia/zh/IPv6.html)
- [https://www.cnnic.net.cn/2/12/index.html](https://www.cnnic.net.cn/2/12/index.html)
- [https://www.ntt-review.jp/archive/ntttechnical.php?contents=ntr201003gls.html](https://www.ntt-review.jp/archive/ntttechnical.php?contents=ntr201003gls.html)
- [https://www.cisco.com/en/US/technologies/tk648/tk872/technologies_white_paper0900aecd8054d37d.html](https://www.cisco.com/en/US/technologies/tk648/tk872/technologies_white_paper0900aecd8054d37d.html)
- [https://en.wikipedia.org/wiki/Happy_Eyeballs](https://en.wikipedia.org/wiki/Happy_Eyeballs)
- [https://www.cnblogs.com/cyx-b/p/14095126.html](https://www.cnblogs.com/cyx-b/p/14095126.html)
- [https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xhtml](https://www.iana.org/assignments/iana-ipv6-special-registry/iana-ipv6-special-registry.xhtml)
- [https://www.iana.org/assignments/ipv6-unicast-address-assignments/ipv6-unicast-address-assignments.xhtml](https://www.iana.org/assignments/ipv6-unicast-address-assignments/ipv6-unicast-address-assignments.xhtml)
- [https://www.iana.org/assignments/ipv6-multicast-addresses/ipv6-multicast-addresses.xhtml](https://www.iana.org/assignments/ipv6-multicast-addresses/ipv6-multicast-addresses.xhtml)
- [https://www.rfc-editor.org/rfc/rfc2460.html](https://www.rfc-editor.org/rfc/rfc2460.html)
- [https://www.networkacademy.io/ccna/ipv6/neighbor-discovery-protocol](https://www.networkacademy.io/ccna/ipv6/neighbor-discovery-protocol)