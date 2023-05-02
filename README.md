Download Link: https://assignmentchef.com/product/solved-coen146l-lab-3-network-commands-and-http
<br>
<h5><strong>Network commands and tools</strong></h5>

<ul>

 <li>Run each of the following basic networking commands in Linux, and write down your observation and explain the usage of the command</li>

</ul>




<ol>

 <li>netstat: displays the contents of network interfaces, with – a option, the command displays the state of all active sockets (more to come on sockets as end points of communication). With – r option, the routing table is displayed. Please type man netstat to learn about all options.</li>

</ol>




<ol>

 <li>ifconfig: configures network interface parameters. With – a option, the state of all interfaces are displayed. Other options are also used to assign a new IP address to an interface, to assign a new network mask for an interface, to disable an interface, and more. Please type man ifconfig to learn about all options.</li>

</ol>




<ol>

 <li>hostname: displays and sets hostname of the system. Please type man hostname to learn about all options.</li>

</ol>




<ol>

 <li>ping: sends ECHO_REQUEST datagram to a network host using ICMP protocol to elicit an ECHO_RESPONSE from the host or gateway. Please type man ping to learn about all options.</li>

</ol>




<ol>

 <li>traceroute: displays the route packets trace to a network host using IP protocol “time to live”. Please type man tracerout to learn about all options.</li>

</ol>




<ol>

 <li>telnet: remote connection to server at a specific port (mainly 80 – http port)</li>

</ol>

<em> </em>

<ol>

 <li>host/dig: performs DNS lookups.</li>

</ol>




<ol>

 <li>route: manipulates network routing tables.</li>

</ol>




<ol>

 <li>arp: displays and modifies the Internet-to-Ethernet address translation tables used by the address resolution protocol.</li>

</ol>




Note: some of the commands may require that you are logged in as a route.




<ul>

 <li>Select three hosts in the internet (one in North America, one in Asia, and one in Europe), and experiment with pinging each host with different packet sizes ranging from 32-bytes to 1048-bytes. For each host,

  <ol>

   <li>identify the packet loss.</li>

  </ol></li>

</ul>




<ol>

 <li>identify the RTT “Round-Trip-Time”.</li>

</ol>




<ol>

 <li>Explain the correlation between these measurements to the geographical location of the hosts.</li>

</ol>




<ul>

 <li>Suppose that the IP address for one of the URL you selected in Step 3 is not cached in your local host, so a DNS lookup is necessary to obtain the IP address. Suppose that three DNS servers are visited before your host receives the IP address from DNS. The first DNS server visited is the local DNS cache, with an RTT delay of RTT0 = 3 msecs. The second and third DNS servers contacted have RTTs of 20 and 26 msecs, respectively. Initially, let’s assume that the Web page associated with the link contains exactly one object, consisting of a small amount of HTML text. Suppose the RTT between the local host and the Web server containing the object is RTTHTTP = 47 msecs.</li>

</ul>




Write a C program that computes the following:




<ol>

 <li>Assuming zero transmission time for the HTML object, how much time elapses from when the client clicks on the link until the client receives the object?</li>

</ol>




<ol>

 <li>Now suppose the HTML object references 6 very small objects on the same web server. Neglecting transmission times, how much time elapses from when the client clicks on the link until the base object and all 6 additional objects are received from web server at the client, assuming non-persistent HTTP and no parallel TCP connections?</li>

</ol>




<ol>

 <li>Assume that the client is configured to support n parallel TCP connections, compute the response time in both persistent and non-persistent cases.</li>

</ol>




<ul>

 <li>Setup a client side to connect to <strong>cs.umass.edu 80</strong>, as follows:</li>

</ul>




<ol>

 <li>Type <strong>telnet gaia.cs.umass.edu 80</strong> to connect to gaia.cs.umass.edu web server<strong>, </strong>explain what happens</li>

</ol>

Note: If you are using MacOS terminal, you may need to install telnet binary file to /usr/local/bin/




<ol>

 <li>Type a GET HTTP request:</li>

</ol>

<strong>GET /kurose_ross/interactive/index.php HTTP/1.1</strong>

<strong>Host: gaia.cs.umass.edu</strong>




Write down your observation.




<ol>

 <li>Analyze the response message sent by the HTTP server, by answering the following questions:</li>

</ol>

 What is the name of the file that is being retrieved in this GET message?




 What version of HTTP is the client running?




 What formats of text and images, if any?




<ul>

 <li>Setup clients to connect to the three hosts you selected in Step 3, then experiment to connect to the public http port 80 and other ports, say: 3389. Write down your observations.</li>

</ul>