# Shell脚本

Shell脚本是一种文本文件，它包含一系列的Shell命令，可以被Shell解释器执行。下面是编写和运行Shell脚本的基本步骤：

1. 编写Shell脚本。使用文本编辑器（如vi、nano等）打开一个新文件，将Shell命令按照顺序写入文件中，以`.sh`为后缀名保存。

例如，一个简单的Shell脚本可以包含以下内容：

```bash
#!/bin/bash
echo "Hello World"
```

2. 赋予Shell脚本执行权限。打开终端，进入Shell脚本所在目录，执行以下命令：

```bash
chmod +x script.sh
```

其中，`script.sh`是您编写的Shell脚本文件名。

3. 运行Shell脚本。在终端中执行以下命令：

```bash
./script.sh
```

即可运行Shell脚本。在这个例子中，Shell脚本会输出字符串"Hello World"。

需要注意的是，Shell脚本中的第一行`#!/bin/bash`是指定Shell解释器的路径，它告诉操作系统使用哪个Shell解释器来执行脚本。在大多数Linux系统中，Bash是默认的Shell解释器，因此使用`#!/bin/bash`即可。如果您使用其他Shell解释器，则需要相应地修改脚本中的第一行。

另外，Shell脚本可以包含变量、条件语句、循环等高级特性，可以根据需要进行编写。