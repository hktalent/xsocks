About
---

XSOCKS is a reliable socks5 proxy server for windows and linux.

It has support forward and reverse mode.

More information about socks5 : [RFC1928](http://www.ietf.org/rfc/rfc1928.txt "RFC1928")
Compiler & Install
---
#####Windows
	devenv.exe build.sln /rebuild RELEASE

#####Linux
	make & sudo make install

Usage
---
		xsocks  [-l port] [-t] [-p1 port] [-p2 port] [-s ip:port]
				[-r ip:port] [-u username] [-p password]

Options
---
		-l  Set forward mode.
		-r  Set reverse mode.
		-t  Build tunnel.
		-s  Redirect another socks server.
		-u  Login username.
		-p  Login password.
		-p1 Accept of XSOCKS client's port.
		-p2 Accept of proxy  client's port.

Examples
---
		xsocks -l 8085 -u root -p 123456
		xsocks -t -p1 8085 -p2 8086
		xsocks -r 192.168.1.10:8085 -u root -p 123456
		xsocks -s 192.168.1.11:8085 -r 192.168.1.10:8086