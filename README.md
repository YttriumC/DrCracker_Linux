# 由于学校更改上网认证方式, 故本项目不再更新
 新的上网认证方式采用网页认证(D版),若想多设备上网可以使用软路由方案,参考xmurp-ua这个项目
 或者使用Privoxy方案,具体可以百度.
 稍微配置下dogcom,任然可用与认证.有时间的话制作一个断网,定时自动认证的软件.


# DrCracker_Linux
 - DrCOM拨号器的Linux版， 在Ubuntu 20.04TLS上实验通过
 - **通过重新编译pppd来达到添加“不可输入字符”（\r\n）的目的**
 - 使用前需安装 rp-pppoe(REHL|CentOS|Fedora...), 或pppoeconf(Debian|Ubuntu...)
 - 其实代码改动不大, 但是编译异常麻烦, 要解决各种依赖, 编译libpcap, openssl等等. pppd之前的代码里没有openssl的源码, 从Github找到后手动添加的.
 - **不建议将其作为突破共享宽带限制使用**
 ## 使用方式
 ### dogcom.conf
 ```
  server = '填上你的Drcom显示的出口IP地址'
  pppoe_flag = '\x2f'
  keep_alive2_flag = '\xdc'
 ```
 ## 友情感谢
  - [mchome/dogcom](https://github.com/mchome/dogcom)
 ## 友情链接
  - [ppp-project/ppp](https://github.com/ppp-project/ppp)
  - [openssl](https://github.com/openssl/openssl)
# 免责声明:
## 本项目仅供教学使用, 严禁用于商业用途.
## 特别指出禁止任何个人或者公司将 DrCracker 的代码投入商业使用，由此造成的后果和法律责任均与本人无关。
## 开源协议: GPLv3.
