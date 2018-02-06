# am-deny-hosts
This application provide a set of shell scripts that helps to protects your linux server from SSH attacks by applying IP block lists to your hosts.deny file. The solution uses minimum resources on your server.

One of the most annoying consequences of operating a public server on the internet is the amount of SSH attacks it will experience. You simply have to view your /var/log/auth.log to see what we mean. Since your server is publicly available you cannot prevent these attacks. What you can do is block them. 

There are a few methods to block IP addresses from accessing your server. These include [Fail2Ban](https://www.fail2ban.org), [DenyHosts](http://denyhosts.sourceforge.net/), [IPTables](https://en.wikipedia.org/wiki/Iptables), and others. The problem with these solutions is that they may be resource intensive and difficult to setup.

The am-deny-hosts application attempts to provide a simple, reliable, and easy to setup solution that can effectively reduce the risk that your server will be compromised by SSH attacks. This solution is also intended to minimize the resource utilization on your server by allowing it to perform its function without wasting CPU cycles analysing your /var/log/auth.log file.  
## How am-deny-hosts works
am-deny-hosts lets you update your /etc/hosts.deny file using downloaded block lists that contain IP addresses of SSH attackers. Your hosts.deny file can up updated periodically by adding a cron job to run the script 
