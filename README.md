<a href="https://github.com/sxdqx/payload_dumper/blob/master/README_EN.md">English language README</a>
# payload dumper
脚本在Linux下的Yandex Amber OTA（完全和增量）上进行了测试（但也可以在Windows上运行）

## 系统要求

- Python3, pip
- google protobuf for python `pip install protobuf`

## 指南

- 确保已安装Python 3.6。
- 下载payload_dumper.py和update_metadata_pb2.py
- 解压缩您的OTA zip并将payload.bin放在这些文件所在的文件夹中。
- 根据您的操作系统打开PowerShell，命令提示符或终端。
- 输入以下命令：python -m pip install protobuf

### 完整的OTA

- 完成后，输入以下命令：python payload_dumper.py payload.bin
- 这将开始将payload.bin文件中的映像提取到您所在的output文件夹中。

### 增量OTA

- 将原始映像（从完整OTA或从设备中转储）复制到old文件夹（文件名称+ .img，例如：boot.img，system.img）
- 运行python payload_dumper.py --diff payload.bin
- 文件提取到您所在的output文件夹中。
