# 复现最新cups-browsed漏洞
https://github.com/OpenPrinting/cups-browsed/security/advisories/GHSA-rj88-6mr5-rcw8#advisory-comment-109538
目前复现程度只达到用github的poc启动打印机服务，然后手动添加这个打印机，添加之后使用这个伪造的打印机去打印东西就会执行特定命令（我这里是id > /tmp/pwn）。实际场景可以考虑伪造（虽然他这个poc的打印机没法直接在cups扫描出来）。不过根据博客原文所说，还可以通过自己构造一个udp包让cups去请求你的伪造打印机来达成目的，就不需要手动添加了。然而这个根据https://github.com/OpenPrinting/cups-browsed/security/advisories/GHSA-rj88-6mr5-rcw8#advisory-comment-109538这个poc没有复现出来。总之先更新或者禁用吧


![image](https://github.com/user-attachments/assets/e8d67aee-5918-454c-9ed1-c46e816aba0b)
