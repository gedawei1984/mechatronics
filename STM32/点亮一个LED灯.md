# 点亮一个LED灯
## 教学目标
1. 学习CUBEMX的基本操作流程

## 学习内容
1. 新建工程。点击File-New Project，在Commercial Part Number处输入芯片型号：STM32F103C8T6，在MCUs/MPUs List处双击芯片型号。
   ![alt text](assets/点亮一个LED灯/image.png)
2. System Core-SYS设置。DEBUG选择Serial Wire。
   ![alt text](assets/点亮一个LED灯/image-2.png)
3. Pin Out View界面，将PC13设置为GPIO_OUTPUT。
   ![alt text](assets/点亮一个LED灯/image-3.png)
4. 在GPIO选项卡中，将PC13的GPIO mode设置为：Output Push Pull。
   ![alt text](assets/点亮一个LED灯/image-4.png)
5. 在Project Manager选项卡中，输入Project Name，ToolChain/IDE选择：MDK-ARM。点击GENERATE CODE，生成代码。
   ![alt text](assets/点亮一个LED灯/image-1.png)
6. 在Keil软件中，先Build，再Load。
   ![alt text](assets/点亮一个LED灯/image-5.png)