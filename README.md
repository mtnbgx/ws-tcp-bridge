ws-tcp-bridge
=============

Project status:
 currently not in use  so i dont know if its up to date with its dependencies. Feel free to use the code as an example however
 the only licensing restriction is let me know if its been helpful! 

A websocket to tcp proxy server, using nodejs which bridges websockets and tcp servers in either direction.

WIP - the actual code is extremely simple, but not tested well (YET), feel free to help.
	  working examples will be provided with some real services when I get time. 
*NOTE* - currently I only support binary ws frames which isnt implemented in alot of browsers...
A workaround is simple to implement.

INSTALL -

nodejs must be installed first before using this server.

#install to current directory
 npm install ws-tcp-bridge
./node_modules/.bin/ws-tcp-bridge

#or install globally
npm install -g ws-tcp-bridge
ws-tcp-bridge

example -

$ ws-tcp-bridge --method=ws2tcp --lport=8080  --rhost=127.0.0.1:8081

proxy mode ws -> tcp
forwarding port 8080 to 127.0.0.1:8081


$ ws-tcp-bridge --method=tcp2ws --lport=8080  --rhost=ws://127.0.0.1:8081

proxy mode tcp -> ws
forwarding port 8080 to 127.0.0.1:8081


If you want to have negotiation of the target address consider forwarding to a socks5 proxy


> forked from andrewchambers/ws-tcp-bridge