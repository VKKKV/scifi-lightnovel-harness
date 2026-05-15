# 六边形编码（Hex Encoding）

用 16 进制（0-9, A-F）表示二进制数据。每字节 = 2 个 hex 字符。常见用途：

- 内存地址：`0x7fff5fbff8c0`
- 颜色值：`#FF5733`（RGB）
- MAC 地址：`00:1A:2B:3C:4D:5E`
- 哈希值：SHA256 输出 `e3b0c44298fc1c14...`
- 二进制文件的 hex dump

在《归零》中，谦治服务器上的文件和目录名全部是 hex 编码。`.meta` 文件提供第一层映射（hex → 实际名称），更深层需要密钥。叶岚在 hex 文件的二进制结构中提取出了内嵌的文本注释。

查看文件 hex 的命令：`xxd file.bin` 或 `hexdump -C file.bin`
