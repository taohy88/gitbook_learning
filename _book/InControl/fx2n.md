# FX2N

```
输入程序后 F4 变换
在写入模式下，写程序以及添加注释
字体缩放，显示--放大缩小
 
MOV 16位数据传送 DMOV 32位数据传送
   例如：MOV K100 D10 将100传送给D10
   通讯中：MOV H0C08B D8120 设备通讯参数 十六进制转换成二进制解析
           16位整数 16进制 C08B 转换成 16位整数 10进制为 -16245
   例如：DMOV D0 D10  将D1 D0 传送给D11 D10 32位整数
 
PLS 上升沿脉冲 上升沿微分输出
    例如 -|X0|- PLS M0 当x0检测到上升沿输出的时候m0为on
 
PLF 下降沿脉冲 下降沿微分输出
     例如 -|X0|- PLF M0 当x0检测到下降沿输出的时候m0为on
 
SET 置位
    例如：SET M0 将MO强制为ON
 
RST 复位
    例如：RST MO 将MO强制为OFF 也可以RST D0 将DO复位为0
 
ALT 交替输出
    例如：alt m0  将M0的输出从ON 改成 OFF
 
CML 反相传送
    例如：CML K1M0 K1MO 将m0的输出自己反相传送
 
INC BIN递增1 DEC BIN递减1
    例如：INC D0 条件满足时，一直累积1
 
FLT BIN整数转换成二进制浮点数
    例如：FLT D8030 D500 将D8030 转换成二进制浮点型D501 D500
 
DECMP 二进制浮点数比较
    例如：DECMP D500 D50 M0 影响3个值MO M1 M2
     如果D500>D50 M0为ON 如果M500=M50 M1为ON 如果M500<M50 M2为ON
 
DEADD 浮点型加法
    例如：DEADD D15 D17 D19
 
DESUB 浮点型减法
    例如：DESUB D15 D17 D19
 
DEMUL 浮点数乘法
    例如：DEMUL D70 D68 D80
 
DEDIV 浮点数除法
    例如：DEMUL D70 D68 D80
 
CALL 子程序调用
     例如：CALL P10
           CALL P11
           -------[FEND]
           P10  子程序1
           -------[RSET]
           P11  子程序2
           -------[RSET]
 
 
时钟寄存器：
D8013 秒 D8014 分 D8015 时 D8016 日
    
特殊寄存器
M8000 初始为上升沿，然后一直保持ON 常闭状态
M8001 初始为下降沿，然后一直保持OFF 常开状态
M8002 初始脉冲，仅在程序一开始为上升沿，然后一直保持OFF 常开状态
M8013 1s时间脉冲继电器 以1 秒为周期振荡
 
主板跟力控通讯
组态里面：FX系列 编程口 通讯参数为 9600 7 偶校验 停止位1
 
 
主板跟MODBUS通讯
D8120 通讯参数寄存器 二进制分析
      H0CO8B 1100 0000 1000 1011
         配置：PLC主机 MODBUS RTU 9600 2位停止位 奇校验Odd 数据长度8位
      H0CO81 1100 0000 1000 0001
         配置：PLC主机 MODBUS RTU 9600 1位停止位 无校验 数据长度8位
      H0408B 0100 0000 1000 1011
         配置：PLC从机 MODBUS RTU 9600 2位停止位 奇校验Odd 数据长度8位
              0100 0000 1000 0001
         配置：PLC从机 MODBUS RTU 9600 1位停止位 无校验none 数据长度8位
 
 
D8121 从机站号寄存器 范围1-247 仅当PLC作为通讯从机使用
D8126 发送前的延时寄存器 范围0-100 单位ms 适当选择5-20ms
当PLC作为主机时：
读取从机数据指令：RD3A K1 H0 D0
     例如 K1 代表从机地址 从1-247
          K4 代表读取的保持寄存器开始地址
          D99 代表读取寄存器的个数 范围1-32
          读取的数据保存在从D100 D101 ...里
 
写入从机数据指令 WR3A K1 H0 D0
D8129 超时时间寄存器 范围0-32767 单位10ms 当接收超时或接收错误时M8129=0N
M8123 一次通信完成标志

主板跟力控通讯
组态里面：FX系列 编程口 通讯参数为 9600 7 偶校验 停止位1
 
 
主板跟MODBUS通讯
D8120 通讯参数寄存器 二进制分析
      H0CO8B 1100 0000 1000 1011
         配置：PLC主机 MODBUS RTU 9600 2位停止位 奇校验Odd 数据长度8位
      H0CO81 1100 0000 1000 0001
         配置：PLC主机 MODBUS RTU 9600 1位停止位 无校验 数据长度8位
      H0408B 0100 0000 1000 1011
         配置：PLC从机 MODBUS RTU 9600 2位停止位 奇校验Odd 数据长度8位
              0100 0000 1000 0001
         配置：PLC从机 MODBUS RTU 9600 1位停止位 无校验none 数据长度8位
 
 
D8121 从机站号寄存器 范围1-247 仅当PLC作为通讯从机使用
D8126 发送前的延时寄存器 范围0-100 单位ms 适当选择5-20ms
当PLC作为主机时：
读取从机数据指令：RD3A K1 H0 D0
     例如 K1 代表从机地址 从1-247
          K4 代表读取的保持寄存器开始地址
          D99 代表读取寄存器的个数 范围1-32
          读取的数据保存在从D100 D101 ...里
 
写入从机数据指令 WR3A K1 H0 D0
D8129 超时时间寄存器 范围0-32767 单位10ms 当接收超时或接收错误时M8129=0N
M8123 一次通信完成标志
```





```
三菱串口通讯：
串口 9600 E 7 1
和校验：(从命令开始相加，低两位16进制 再转换成 ASCII码 数字加30H 字母加37H）
读取D数据：
      PC发送：开始 命令 首地址 位数（字节数） 终止 和校验
      例如：读取d123开始4个字节 即d123 d124 低字节在前高字节在后16进制整数
              02 30 31 30 46 36 30 34 03 37 34
      三菱返回：开始 数据1 数据2 --数据n 终止 和校验
      例如： d123 数据为2 d124 数据为3  
              02 30 32 30 30 30 33 30 30 03 38 38  
 
写入D数据：
      PC发送：开始 命令 首地址 位数（字节数）数据  终止 和校验
      例如：读取d123开始4个字节 即d123=1234 d124 =ABCD
              02 31 31 30 46 36 30 34 33 34 31 32 43 44 41 42 03 34 39
      三菱返回：06 接受正确 15 接受错误
 
置位：地址倒过来 给m0 +800H=0800H
02 37   30 30 30 38   03 30 32
复位：
02 38   30 30 30 38   03 30 33
 
读取X0-X7 +80H=0080H
02 30   30 30 38 30  30 31   03 35 43
返回：02   30 30   03 36 33  
 
读取Y0-Y7 +A0H =00A0H
02 30 30 30 41 30 30 31 03 36 35
返回
02  43 30  03 37 36----C 0   1100 0000 y7-y4 y3-y0
 
02 31 31 30 46 36 30 32 30 30 30 31 03 33 34 写d123 256
 
 
FFFF FFFF FFFF C08B
FFFF FFFF FFFF FFFF
```
