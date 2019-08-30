添加
firewall-cmd --zone=public --add-port=80/tcp --permanent    （--permanent永久生效，没有此参数重启后失效）
重新载入
firewall-cmd --reload
查看
firewall-cmd --zone= public --query-port=80/tcp
删除
firewall-cmd --zone= public --remove-port=80/tcp --permanent


查看所有打开的端口： 
firewall-cmd --zone=public --list-ports



iptables的配置
-A INPUT -m state --state NEW -m tcp -p tcp --dport 6379 -j ACCEPT
