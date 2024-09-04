分支说明：
odhcp6c：允许请求特定的 ipv6 前缀（WAN口）
使用可选的精确 ipv6 前缀格式扩展 -P 选项。
这允许在某些情况下保留 IPv6 前缀，例如
如果前缀是在上游动态发出的。

示例：
-P <长度>
-P <前缀/长度>

用法参考：https://www.v2ex.com/t/1069456?p=1

1. 静态编译了 odhcp6c x86 版本，替换/usr/sbin 下面同名文件。
2. 修改/lib/netifd/proto/dhcpv6.sh 里面的 reqprefix 变量，如 2409:xxxx:xxxx:100::/60 。
3. 重新拨号即可。
