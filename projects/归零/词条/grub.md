# GRUB（GRand Unified Bootloader）

Linux 系统的启动引导器。开机时 BIOS/UEFI 加载 GRUB → GRUB 加载内核 → 内核启动操作系统。

常见故障：
- `grub rescue>` 提示符：GRUB 找不到启动分区——通常是因为硬盘分区表变化、GRUB 配置文件损坏、或系统被擦除后 GRUB 残留
- 修复方法：用 live USB 启动 → chroot 进原系统 → `grub-install && update-grub`

在《归零》Ch1 中，林奕在杂货店买到的 P53 就卡在 `grub rescue>`。这暗示前主人（waterlily/遥）可能在临终前擦除了系统——或者系统在某个时刻自行重置了。
