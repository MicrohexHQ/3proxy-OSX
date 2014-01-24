/*
   3APA3A 3proxy tiny proxy server
   (c) 2002-2007 by ZARAZA <3APA3A@security.nnov.ru>,
		 Vladimir Dubrovin <vlad@sandy.ru>

   please read License Agreement

   $Id: Readme,v 1.7 2009/03/18 17:00:11 vlad Exp $
*/

Please read doc/html/index.html and man pages.

3proxy    	Combined proxy server may be used as
		Windows 95/98/NT/2000/XP/2003/Vista
		executable or service (supports installation and removal).
		It uses config file to read it's configuration (see
		3proxy.cfg.sample for details).
		--install installs and starts proxy as NT/2000/XP service
		(config file should be located in the same directory)
		--remove removes the service (should be stopped before via
		net stop 3proxy).
		3proxy.exe is all-in-one, it doesn't require all others .exe
		to work.
		See 3proxy.cfg.sample for examples, see man 3proxy.cfg
proxy    	HTTP proxy server, binds to port 3128
ftppr    	FTP proxy server, binds to port 21
socks    	SOCKS 4/5 proxy server, binds to port 1080
ftppr		FTP proxy server, please do not mess it with FTP over HTTP
		proxy used in browsers
pop3p    	POP3 proxy server, binds to port 110. You must specify
		POP3 username as username@target.host.ip[:port]
		port is 110 by default.
		Exmple: in Username configuration for you e-mail reader
		set someuser@pop.somehost.ru, to obtains mail for someuser
		from pop.somehost.ru via proxy.
smtpp    	SMTP proxy server, binds to port 25. You must specify
		SMTP username as username@target.host.ip[:port]
		port is 25 by default.
		Exmple: in Username configuration for you e-mail reader
		set someuser@mail.somehost.ru, to send mail as someuser
		via mail.somehost.ru via proxy.
icqpr    	ICQ/AIM proxy. Maps some TCP port to TCP port of ICQ
		server and performs packets translation. Example:
		icqpr 5190 login.icq.com 5190
msnpr		MSN proxy (beta)
tcppm    	TCP port mapping. Maps some TCP port on local machine to
		TCP port on remote host.
udppm    	UDP port mapping. Maps some UDP port on local machine to
		UDP port on remote machine. Only one user simulationeously
		can use UDP mapping, so it cann't be used for public service
		in large networks. It's OK to use it to map to DNS server
		in small network or to map Counter-Strike server for single
		client (you can use few mappings on different ports for
		different clients in last case).
mycrypt    	Program to obtain crypted password fro cleartext. Supports
		both MD5/crypt and NT password.
			mycrypt password
		produces NT password
			mycrypt salt password
		produces MD5/crypt password with salt "salt".
dighosts    	Utility for building networks list from web page.
countersutil	Utility to manage counters file


Run utility with --help option for command line reference.

Latest version is available from http://3proxy.ru/
