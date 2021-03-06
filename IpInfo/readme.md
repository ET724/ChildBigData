

**机器：**

- 192.168.101.48
- 192.168.101.49
- 192.168.101.50

**openvpn分配：**

- 当openvpn不使用时可以关闭连接，使用时再进行连接即可

| vpn   | people |
| ----- | ------ |
| vpn81 | 张继珂 |
| vpn82 | 李可   |
| vpn83 | 于泽洋 |
| vpn84 | 章策   |

**ip对应node：**

每一台的用户名：`suncaper` 密码：`suncaper2020`

~~~ txt
192.168.101.48 node-master
192.168.101.49 node1
192.168.101.50 node2
~~~

**使用方法：**

1. 启动openVPN(需要配置好上面分发的opvn文件，具体配置见视频)

   - 现在相当于连接到了实训公司的一个内部网络，所以可以之后使用局域网的地址段192.168.101.xx 但是我觉得如果你自己的主机本来的ip就是这几个或者局域网中含有这几个的ip，那么可能会出现冲突
  - 由于使用hadoop webui下载文件可能会不能下载，因为无法解析node1的域名的ip地址，所以为了方便，还是可以在hosts里加上三条映射的
   - 当使用openVPN时访问其他网页可能受限，例如钉钉视频的速度就受到影响

2. 使用filezila或其他工具来传递文件（:red_circle:禁止:red_circle:；非我本人允许不要乱传文件，以面干扰工作​ ）

3. 使用xshell连接各个节点

   我个人的连接名称

   | name                     | ip/主机        |
   | ------------------------ | -------------- |
   | ChildBigData-node-master | 192.168.101.48 |
   | ChildBigData-node1       | 192.168.101.49 |
   | ChildBigData-node2       | 192.168.101.50 |

4. 在窗口中进行命令操作

   - :red_circle:禁止进行允许列表外的操作:red_circle:
   - :red_circle:非我本人允许不要更改环境变量、软件配置等:red_circle:
   - 允许操作列表：
     - 执行 `hive` 命令，在之后的hive命令窗口中进行数据库操作练习，联系完毕后使用 `quit` 退出

访问webUI页面

1. 直接在游览器中输入：

   - http://192.168.101.48:50070/ 
   - http://192.168.101.48:8088/cluster

   :warning:不建议修改windows的host文件来使用域名访问，因为这只是这一个月的暂时性的使用，之后不用了干其他事可能会出问题，所以就用ip访问吧

   :warning:此使必须让openVPN处于打开状态才能访问

