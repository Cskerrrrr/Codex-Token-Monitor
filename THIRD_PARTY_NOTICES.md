# 第三方组件与动态运行库

应用代码采用原生编译。以下未修改的第三方组件保留各自许可证；未限制用户根据第三方许可证修改、替换、调试这些组件的权利。

| 组件 | 版本 | 许可 / 对应源码 |
|---|---|---|
| Python | 3.12.14 | [PSF 许可及源码](https://www.python.org/downloads/release/python-31214/) |
| Qt | 6.11.2 | LGPL-3.0；[完整源码](https://download.qt.io/official_releases/qt/6.11/6.11.2/single/) |
| PySide6 / Shiboken6 | 6.11.2 | LGPL-3.0；[对应源码](https://download.qt.io/official_releases/QtForPython/pyside6/PySide6-6.11.2-src/) |
| Cryptography | 50.0.1 | Apache-2.0 / BSD-3-Clause；[源码](https://github.com/pyca/cryptography/tree/50.0.1) |
| CFFI | 2.1.1 | MIT；[源码](https://github.com/python-cffi/cffi/tree/v2.1.1) |
| Zstandard | 0.25.0（Python 绑定） | BSD；[源码](https://github.com/indygreg/python-zstandard/tree/0.25.0) |

发布页面的 `CodexTokenMonitor-portable.zip` 提供完整的动态链接版本与 `licenses` 目录。Qt Core / Gui / Widgets / Network 通过独立 DLL 加载，未静态链接到应用中。

## 替换或调试 LGPL 组件

退出程序后，解压便携包。可将其中 PySide6、Shiboken6 对应目录中的 DLL / PYD 替换为自行编译、同架构并保持二进制兼容的版本，再运行根目录的 `CodexTokenMonitor.exe`。组件路径保持原样；调试修改的组件时可以关闭自动更新。应用没有禁止这一操作，也未加入检测调试器后拒绝运行的限制。

上表给出本次分发所用组件的对应源码位置，与安装包同时提供获取说明。各组件的版权声明和完整许可证随包保留。
