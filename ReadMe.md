<p align="center">
  <h3 align="center">LCUI</h3>
  <p align="center">
    面向 C 的图形界面开发库，可借助 XML 和 CSS 构建简单的跨平台桌面应用
  </p>




VS2013 编译通过
编译目标 Visual Studio 2013 - Windows XP (v120_xp)

使用的版本：20180304
  https://github.com/lc-soft/LCUI/tree/9995b23bebb643cf1e74c544922db5028ef4eae7

解决一下问题
  1、添加编译的各种开源库,LCUI-develop\src\main.c。
  
  2、LCUI_PreInitWinApp符号找不到。windows_events.c添加头文件
  #include "../../../Include/LCUI/platform/windows/windows_events.h"
  
  3、恢复生成文件的输出路径为默认，避免文件找不到
  
  4、找不带debug信息，Linker --> Debugging --> Generate Debug Info，设置为Yes。

  5、hello world 闪退，Debuging --> Working Directory --->$(OutDir)

编译说明：
  打开 LCUI-develop\build\windows\LCUI-Demo.sln


![ScreenShot](/ScreenShot.png)


From
  https://github.com/lc-soft/LCUI

