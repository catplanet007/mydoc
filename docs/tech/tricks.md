---
sidebar_position: 1
---

### 备份网站

```bash
wget --restrict-file-names=windows -m -k -p -c --domains=coolshell.cn https://coolshell.cn/
```

- `-m`：用于进行镜像备份，尽可能地复制整个网站的结构和内容
- `-k`：将绝对链接转换为相对链接，以便在离线浏览时保持页面内链接的正确性
- `-p`：下载页面所需的所有文件，包括图像、样式表和脚本等
- `-c`：如果下载过程中断，进行断点续传，下次执行命令时会从上次中断的地方继续下载
- `--restrict-file-names=windows`：确保文件名在不同操作系统下都能正确处理
- `--domains`：指定只下载特定域名下的内容
- `--exclude-directories`：排除某些目录不进行下载，比如：
  - `wget -m -k -p --exclude-directories=/dir1,/dir2 [网站 URL]`
- `--limit-rate`：限制下载速度
  - `wget -m -k -p --limit-rate=100k [网站 URL]`

### grep 二进制文件中文本

二进制文件中有部分文本。

```bash
strings trace.dat | grep do_sys_open 
```

### 有权限却无法写入

```bash
$ sudo echo do_sys_open > /sys/kernel/debug/tracing/set_graph_function
-bash: /sys/kernel/debug/tracing/set_graph_function: Permission denied

# 换成
$ echo do_sys_open | sudo tee /sys/kernel/debug/tracing/set_graph_function
# 或
$ sudo sh -c "echo do_sys_open > /sys/kernel/debug/tracing/set_graph_function"
```

### 让 man 手册支持鼠标滚轮
```bash
$ export MANPAGER="less -X"
```
缺点是需要先使用空格向下翻页多次后，才可使用鼠标滚轮上下滚动。

另一种方式是：
```bash
$ export LESS='-R -M --mouse'
```
这种方法缺点是无法支持鼠标选中复制了，滚动也有点慢。
