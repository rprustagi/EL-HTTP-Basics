# EL-HTTP-Basics
The example and code snippets correspond to the article "Exploring Basics of the HTTP Protocol" 
in the inaugural edition of ACCS Journal "Advanced Communications and Computing" volume 01, issue 01, 2017.

## ACCS-EL-HTTP-Basics.pdf\
	The PDF version of the article as appeared in ACCS Magazine
"Advanced Communications and Computing", Vol 01, Issue 01.

The examples as shown in the tables in this article are
listed below. The description of each is given below. These examples assume that hostname
*myweb.com* is resolvable to IP address for network communication to work. To ensure this,
please ensure to make an entry in the file */etc/hosts* of computer running the web server
e.g. *Apache* web server.

**welcome.pcap**:\
        This file contains the wireshark capture of a web request when a simple web page
        *welcome.html* is access in browser. To see the entire communication between a web brwoser and web server when accessing the web page *http://myweb.com/welcome.html*, open this file in *wireshark* and it will show all the packet exchange including TCP/IP protocol stack, HTTP headers (both request and response) as well as the content of web page.

**Table1-HTTP-Request.txt**:\
        Contains the *Request line and the *request headers* sent by the web client e.g.
        web browser, when access URL *http://myweb.com/welcome.html*.

**Table2-HTTP-Response.txt**:\
        Contains the *Status line and the *Response headers* sent by the web server  e.g.
        Apache, when a browser accesses URL *http://myweb.com/welcome.html*.

**Table3-welcome.html**:\
        Contains the contents of webpage *welcome.html* deployed at web server e.g.
        *Apache*.

**Table5-Req-Badheader.txt**:\
        This is the content of web request with bad headers.
        When using this with *telnet* command, please ensure to provide one empty line at
        the end to indicate end of request headers. This can be used with *nc* as follows.
        *cat Table5-Req-Badheader.txt | nc myweb.com 80*

**Table6-Resp-BadHeader.txt**:\
        This is the content of web response when web request contains *bad* HTTP Request headers.

