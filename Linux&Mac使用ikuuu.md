---
layout: cover
---

# Linux 使用 ikuuu

Use ikuuu just like Android in Linux.

---

## 安装-安装必要部分和脚本测试

1. 按照[官方教程](https://ikuuu.art/user/tutorial?os=linux&client=clash)的方法安装好必要部分
2. 假设安装在 /home/user/documents/clash 下
3. 则该目录下应该有一个命名为 clash 的文件
4. 在任意其他位置新建一个文本文件命名为 `clash`, 并输入以下内容:

   ``` bash
   #!/bin/bash
   cd /home/user/documents/clash
   clash -d .
   ```

5. 赋予该文件可执行权限: `chmod +x clash`
6. 测试一下: `./clash`
7. 成功的话, 应该会看到 `clash` 运行的 IP 和端口等信息

---

## 安装-配置命令行

1. 将该文件移动到 `/usr/local/bin` 或 `/usr/bin` 等环境变量包括的路径（终端输入 `env` 查询）下

   ``` bash
   sudo cp ./clash /usr/local/bin
   ```

2. 测试一下，终端输入 `clash`
3. 成功的话, 应该会看到类似步骤 7 的内容，美滋滋
