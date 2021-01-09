# videoRecording
video recording with the tools from opencv

使用方法:
1.创建bin、video、build文件夹并编译，在bin目录中生成可执行文件。
```
mkdir bin && mkdir video
mkdir build && cd build
cmake ..
make
```
2.在src中的源代码中找到`#define name`,修改为你想要的名字，注意文件路径不要动。找到`VideoCapture cap(0);`，cap()中的数字代表设备序号，一般0为笔记本自带摄像头，1为外接摄像头
3.在bin中
```
./videoRecorder
```
开始录制，命令行显示当前帧数
`ctl + c`结束录制
4.生成的视频在video目录中，注意每次录制新的视频要回去改define的名字，不然录不上。
