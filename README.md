# DrCracker_Linux
 - DrCOM拨号器的Linux版， 在Ubuntu 20.04TLS上实验通过
 - **通过重新编译pppd来达到添加“不可输入字符”（\r\n）的目的**
 - 使用前需安装 rp-pppoe(REHL|CentOS|Fedora...), 或pppoeconf(Debian|Ubuntu...)
 - 其实代码改动不大, 但是编译异常麻烦, 要解决各种依赖, 编译lipcap, openssl等等. pppd之前的代码里没有openssl的源码, 从Github找到后手动添加的.
 ## 使用方式
 ### dogcom.conf
 ```
  server = '填上你的Drcom显示的出口IP地址'
  pppoe_flag = '\x2f'
  keep_alive2_flag = '\xdc'
 ```
 ## 友情感谢
  - [mchome/dogcom](https://github.com/mchome/dogcom)
# 免责声明:
## 本项目仅供教学使用, 严禁用于商业用途.
## 特别指出禁止任何个人或者公司将 DrCracker 的代码投入商业使用，由此造成的后果和法律责任均与本人无关。
## 开源协议: GPLv3.
