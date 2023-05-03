# 从源码编译安装opencv-python

1. 确保您的系统已安装必要的构建工具和依赖项。例如，在Ubuntu上，可以使用以下命令安装：

```bash
sudo apt-get update
sudo apt-get install build-essential cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
```

这个命令将在Ubuntu系统上安装一些必要的构建工具和依赖项，包括：

- build-essential：Ubuntu系统的基本构建工具，包括编译器和链接器等。
- cmake：一个跨平台的开源构建工具，可用于自动生成Makefile文件。
- git：一个版本控制系统，用于从GitHub上克隆OpenCV源代码。
- libgtk2.0-dev：GTK+ GUI工具包的开发文件，用于构建OpenCV的GUI组件。
- pkg-config：用于在编译时获取库的元数据信息。
- libavcodec-dev：FFmpeg的编解码库的开发文件，用于处理视频和音频流。
- libavformat-dev：FFmpeg的多媒体容器格式的开发文件，用于读取和写入视频和音频文件。
- libswscale-dev：FFmpeg的图像缩放和色彩空间转换的开发文件，用于处理视频帧。

2. 从OpenCV的GitHub存储库中克隆源代码：

```bash
git clone https://github.com/opencv/opencv.git
```

3. 切换到下载的源代码目录：

```bash
cd opencv
```

4. 创建一个用于构建的新目录：

```bash
mkdir build
cd build
```

5. 运行cmake命令来配置编译环境。在这个过程中，您可以指定一些选项来启用或禁用某些功能：

```bash
cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..
```

这个cmake命令的作用是配置OpenCV的构建选项，其中包括：

- `-D CMAKE_BUILD_TYPE=RELEASE`：指定OpenCV的构建类型为“RELEASE”，这将启用一些优化选项以提高性能。
- `-D CMAKE_INSTALL_PREFIX=/usr/local`：指定OpenCV的安装目录为`/usr/local`，这将安装OpenCV到系统的标准位置之一，以便在整个系统中使用。
- `..`：指定源代码的上级目录作为CMakeLists.txt的位置。

这个命令将根据配置文件生成一个Makefile，可以使用`make`命令编译OpenCV。

6. 接下来，使用以下命令编译源代码：

```bash
make -j8
```

7. 编译完成后，使用以下命令安装OpenCV：

```bash
sudo make install
```

8. 最后，使用以下命令安装Python绑定：

```bash
pip install opencv-python
```

这将从PyPI上安装opencv-python包，其中包含OpenCV Python绑定。

完成上述步骤后，您现在应该已经成功地从源代码编译安装了opencv-python。