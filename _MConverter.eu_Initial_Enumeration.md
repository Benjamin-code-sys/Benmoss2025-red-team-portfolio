**Initial Enumeration**

• Let's begin with basic reconnaissance. When we scan real-world targets with tools like network scanners and web crawlers, it's generally considered good practice to execute them in as limited a scope as possible to avoid overloading any systems. 

• Since we are only dealing with three systems \(192.168.120.130-132\), we'll scan the top 1000 ports with nmap: 1/3





• The output shown in Listing 1 indicates that we are dealing with a Windows environment, and specifically an Act-ive Directory infrastructure containing an "evil.com" domain and a DC02 host acting as the domain controller. In addition, the scan reveals two servers named web01 and file01. 

• Remote Desktop is running on all three targets and although we could brute-force them, this is not a common find during an external penetration test. However, web01 exposes access to an IIS web server on TCP port 80, which is a more appropriate first vector for our case study. 

• Let's begin by browsing the web server. 

2/3

• As shown, this web application allows file uploads. If configured incorrectly, this could provide the initial foothold we need. 

• Admittedly, a web site that allows unauthenticated file uploads is rather unrealistic. However, there are innumerable initial vectors and the primary focus of this module is chaining attacks and putting together the concepts we have discussed in previous modules. 

• Since we are targeting so few machines, we will pause our enumeration to focus on this potential vulnerability. 

3/3



