# 5 SPI
## 第18课 [SPI]总线结构
1. SPI共包含4根信号线
   1. MOSI：主站输出、从站输入
   ![alt text](<assets/5 SPI/image-1.png>)
   2. MISO：主站输入、从站输出
   ![alt text](<assets/5 SPI/image-2.png>)
   3. SCK：时钟信号，一个时钟脉冲发送一位数据
   ![alt text](<assets/5 SPI/image-3.png>)
   4. NSS：低电平片选信号
   ![alt text](<assets/5 SPI/image-4.png>)
2. 接线图
   ![alt text](<assets/5 SPI/image-5.png>)
3. 通信过程
    1. NSS拉低电平，选择想要的从机。
    2. 随着SCK的时钟脉冲，主站和从站之间传输信息。
    ![alt text](<assets/5 SPI/image-6.png>)
## 第19课 [SPI]5个参数
1. 波特率。按照以下原则选取。
   1. 允许的最大值
   2. 设备承受的极限
   3. 电路允许的极限
2. 比特位传输顺序。根据从站设备选择。
   1. MSB：高位先传送，Most Significant Bit
   2. LSB：低位先传送，Least Significant Bit
3. 数据帧长度：8位一组，或者16位一组。根据从站选择。
4. 时钟的极性。空闲时SCK的电压状态。
5. 时钟的相位：第一边沿采集，或者第二边沿采集。
6. 时钟模式：根据时钟的极性和相位，分为以下四种。
   ![alt text](<assets/5 SPI/image-7.png>)
## 第20课 [SPI]按钮实验
### 按钮编程技巧
#### 控制要求：每次松开按钮的时候，翻转灯的状态。
1. 电路图
   ![alt text](<assets/5 SPI/image-9.png>)
2. 检测按下还是松开。定义两个变量pre和cur，通过不断检测pre的值和两个变量是否相同，判断按钮是按下还是松开。
   ![alt text](<assets/5 SPI/image-8.png>)
3. 翻转灯的状态
   ![alt text](<assets/5 SPI/image-10.png>)
4. 软件防抖。捕捉到变化后，延迟10ms，再判断。
   ![alt text](<assets/5 SPI/image-11.png>)
## 第21课 [SPI]外部flash实验
## 第22课 [SPI]flash数据存取