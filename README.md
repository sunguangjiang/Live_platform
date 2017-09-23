### Live_platform
    ` Simply Live PlatForm :) `
    - [Frame]           : *Qt 5.7*
    - [Language]        : *C++*
    - [Lib]             : *STL*
    - [SimplyStructure] : *C/S*
    - [Protocol]        : *TCP/IP & UDP*
    - [Fuction]         : *Live(Video & Audio)* *Watching Live* *Barrage* *Gift*
    - [DataBase]        : *Sqlite3*
    - [Sever Function]  : *Heartbeats* 
    - [Client Function] : *Sign up/in* *Open Live* *Send Barrage* *Send gift*
   
   ------------------------------------------------------------------------------------------------------------
    1.项目使用 C/S 架构，分为两个文件夹， Server 、Client ;
    2.服务器数据存储使用 Sqlite3 数据库，目前分为 userInfo(用户账号密码基本信息)、userIndex(用户积分消费额等信息)、userOL(在线用户列表临时存储)、roomInfo(直播间基本信息包括直播间名及直播间UDP地址、房主名);
    3.服务器IP地址使用 LocalHost，端口监听 AnyIPv4；
    4.服务器使用日志输出至 log.txt，方便后期校验；
    5.客户端通过 TCP/IP 链接至服务器端，可完成注册、登录功能（重复注册、重复登录、错误密码等情况均有相应提示），功能来自于数据库操作；
    6.客户端登录成功后，用户将拥有观看直播和创建直播间功能，其中UDP广播地址为随机生成，端口号为指定端口传输视频流、音频流；
    7.客户端用户创建直播间功能通过TCP/IP协议与服务器连接，向服务器发送直播间基本信息：UDP地址、直播间名、直播间拥有者名字；
    8.客户端用户在第二个窗口界面可以刷新直播间列表，服务器会即时发送正在直播的房间名、UDP地址等信息至客户端，用户双击List中房间名即可建立UDP连接；
    9.客户端无论是进入直播间观看还是开启直播间进行直播，均可以发送实时弹幕，全直播间的用户均能接收到弹幕信息，并可以在视频界面滚动播放.
    
