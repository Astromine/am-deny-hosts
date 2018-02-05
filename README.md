# am-deny-host
Protects your linux server from SSH attacks by applying IP block lists to your hosts.deny file with minimum resource utilization.

One of the most annoying consequences of operating a public server on the internet is the amount of SSH attacks it will experience. You simply have to view your /var/log/auth.log to see what we mean. Since your server is publicly you cannot prevent these attacks. What you can do is block them. 
