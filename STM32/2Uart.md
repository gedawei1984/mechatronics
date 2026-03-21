# Uart
## 第11课 [UART]基础知识
1. 串口通信的数据帧。由起始位、数据位、停止位组成。
2. 起始位：高电平下拉低电平保持一位，代表起始位。
3. 数据位：8位或者9位，包含或者不包含1位校验位。校验分为奇校验或者偶校验。
4. 停止位：上拉高电平保持一位，代表停止位。
5. 波特率：9600或者115200等。9600代表每秒传输9600位，每位传输需要1/9600秒，约为0.1毫秒。115200每位约需要8.7微妙。
6. 接线：TX发送（Transmit），RX接收（receive）。一端的TX接另一端的RX。
## 第12课 [UART]简单数据发送实验
### HAL库函数
串口发送函数
```c
HAL_UART_Transmit(UART_HandleTypeDef *huart, uint8_t *pData, uint16_t Size, uint32_t Timeout)
```
举例：
```c
HAL_UART_Transmit(&huart1, &a, 1, HAL_MAX_DELAY);
```
其中：huart1是串口1的句柄，配置好后系统自动生成的。a是变量，&a是变量的地址;1是发送1位数据，HAL_MAX_DELAY是一直等待发送完毕。

### 简单数据发送实验：
1. MX设置：
   1. Connectivity中，Usart1设置为Asynchronous模式。
   2. Usart1的Parameter Settings设置为：115200，8，None，1。
2. 串口调试助手：
   1. 设置115200，8，N，1。
   2. 打开串口
3. 核心程序：
   ```c
    //在while循环上面添加以下程序
    uint8_t byteNumber = Ox5a;
    uint8_t byteArray[] = {1,2,3,4,5};
    char ch= 'a’;
    char *str = "Hello world";
    HAL_UART_Transmit(&huart1, &byteNumber, 1, HAL_MAX_DELAY);//发送字节0x5a
    HAL_UART_Transmit(&haurt1, byteArray, 5, HAL MAX DELAY);//发送字节数组{1,2,3,4,5｝
    HAL_UART_Transmit(&haurt1, (uint8 t *)&ch, 1, HAL_MAX_DELAY);//发送字母
    HAL_UART_Transmit(&haurt1, (uint8 t *)str, strlen(str), HAL MAX DELAY);//发送字符串
    while(1){
    ......
    }
   ```
4. 调试：在Keil中，点击放大镜进入调试。先运行到curse line，然后单步运行，查看串口调试助手接收到的数据。
## 第13课 [UART]简单数据接收实验
### HAL库函数
### 简单数据接收实验