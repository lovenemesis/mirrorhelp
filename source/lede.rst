=======================
OpenWRT/LEDE 源使用帮助
=======================

地址
====

https://mirrors.ustc.edu.cn/lede/

说明
====

OpenWRT/LEDE 下载站镜像。

这是对 https://openwrt.org/ 的完整镜像，内容包括官方支持的平台的 ROM、SDK 及工具链、软件仓库镜像等。

使用说明
========

一般情况下，下载来自 ``downloads.openwrt.org`` 的文件时，将 URL 中的这部分域名替换为 ``mirrors.ustc.edu.cn/lede`` 即可。

如要使用本镜像作为 OpenWRT/LEDE 系统 opkg 软件仓库，SSH 登录路由器编辑 :file:`/etc/opkg/distfeeds.conf` 文件，同样按照上面的方法替换域名即可。可以使用如下命令操作：

::

    sed -i 's/downloads.openwrt.org/mirrors.ustc.edu.cn\/lede/g' /etc/opkg/distfeeds.conf

之后运行 `opkg update` 更新软件索引，注意检查是否出现错误。

.. tip::
    使用 HTTPS 可以有效避免国内运营商的缓存劫持，但需要另行安装 ``libustream-openssl ca-bundle ca-certificates`` 。

相关链接
========

:官方主页: https://openwrt.org/
:OpenWRT 文档: https://openwrt.org/docs/start
:OpenWRT 论坛: https://forum.openwrt.org/
