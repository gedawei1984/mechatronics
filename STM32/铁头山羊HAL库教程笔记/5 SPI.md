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
1. 波特率
2. 比特位传输顺序
3. 数据帧长度
4. 时钟的极性
5. 时钟的相位
## 第20课 [SPI]按钮实验
### 按钮编程技巧
1. 检测按下还是松开
2. 软件防抖
### 按钮实验
#### 控制要求
## 第21课 [SPI]外部flash实验
## 第22课 [SPI]flash数据存取