# MAC 地址（Media Access Control）

网络接口卡的硬件地址——48 位十六进制数，全球唯一（理论上）。格式如 `00:1A:2B:3C:4D:5E`。前 24 位是厂商 OUI（Organizationally Unique Identifier），后 24 位由厂商分配。

在《归零》中，wl0 的 MAC 地址末尾编码了一个日期——2019 年 12 月 24 日。林奕通过 MAC 地址发现了这个时间戳，这是他认为 wl0 不只是普通网卡的第一个线索。

查看 MAC 地址的命令：`ip link show wl0`
