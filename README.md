
### PosiStageNet Protocol v2.0, November 4th 2014
`Copyright (c) 2014 VYV Corporation`

---

这个包包含PosiStageNet协议的文档和c++工程。.
它还包含三个简单的演示，演示如何从服务器端或客户端的使用工程.

工程中只使用 **'.hpp'** 文件. 如果您想在您的项目中使用这个工程,
必须包含 **"psn_lib.hpp"** 文件在你的 **".cpp"** 工程内.  

该工程是跨平台的，因此可以在Windows、Linux和Mac OS X下编译.
演示项目将只在Windows操作系统下工作，因为他们使用特定于Windows的实现.
一个简单的 **udp_socket class**. 如果希望在另一个平台上运行这些演示程序，则需要编写自己的 **udp_socket class**.

---

#### 更新日志
`Version 2.02 - 2018-01-03`

* Bug:
  * Description: psn_tracker class constructor always was setting its member 'validity' to 0, ignoring the given parameter
  * Fix: The constructor now uses the given parameter to initialize the member 'validity'.
* Bug:
  * Description: The frame_id needed to be sequential. If not, a frame could be lost when reconstructing frame packets.
  * Fix: Frame IDs can now follow any sequence, as long as two consecutive frames have different IDs. 
