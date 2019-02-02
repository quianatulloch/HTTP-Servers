# HTTP & Web Servers
An HTTP transaction always involves a client and a server. You're using an HTTP client right now — your web browser. HTTP was originally created to serve hypertext documents, but today is used for much more.

A server is just a program that accepts connections from other programs on the network. When you start a server program, it waits for clients to connect to it. Then when a connection comes in, the server runs a piece of code — like calling a function — to handle each incoming connection. A connection in this sense is like a phone call: it's a channel through which the client and server can talk to each other. Web clients send requests over these connections, and servers send responses back.

**404** is the HTTP status code for "Not Found".

# Parts of a URI
A web address is also called a URI for Uniform Resource Identifier. From a web user's view, a URI is a piece of text that you put into your web browser that tells it what page to go to. A URI is a name for a resource — such as a Wikipedia article, or a data source like the Google Maps API. URIs are made out of several different parts, each of which has its own syntax.

Here is an example of a URI: 

~~~ 
https://en.wikipedia.org/wiki/Fish
~~~
This URI has three visible parts, separated by a little bit of punctuation:

  * **https** is the scheme;
  * **en.wikipedia.org** is the hostname;
  * **/wiki/Fish** is the path
  
**Scheme**

The first part of a URI is the scheme, which tells the client how to go about accessing the resource. Some URI schemes you've seen before include **http**, **https**, and **file**.
  
HTTP and HTTPS URIs look almost the same. The difference is that when a client goes to access a resource with an HTTPS URI, it will use an encrypted connection to do it. Encrypted Web connections were originally used to protect passwords and credit-card transactions, but today many sites use them to help protect users' privacy.

**Hostname**

In an HTTP URI, the next thing that appears after the scheme is a hostname — something like www.udacity.com or localhost. This tells the client which server to connect to. A hostname can only appear after a URI scheme that supports it, such as http or https. In these URIs, there will always be a :// between the scheme and hostname.

**Path**

The path tells the server which resource the client is looking for. The server interprets the path to figure out what resource to send. In the case of a search query, it sends back a search result page that maybe never existed before. When you write a URI without a path, such as http://udacity.com, the browser fills in the default path, which is written with a single slash. That's why http://udacity.com is the same as http://udacity.com/.

with a single slash. That's why http://udacity.com is the same as http://udacity.com/ (with a slash on the end). The path written with just a single slash is also called the root. It's the root of the resources served by the web server. 
## Relative URI references
~~~
<a href="cliffsofinsanity.png">cliffsofinsanity.png</a>
~~~
URIs like this one don't have a scheme, or a hostname — just a path. This is a relative URI reference. It's "relative" to the context in which it appears — specifically, the page it's on. This URI doesn't include the hostname or port of the server it's on, but the browser can figure that out from context. 

**Other URI parts**

If you follow these links in your browser, it will fetch the same page from Wikipedia's web server. But the second one displays the page scrolled to the section about the discovery of oxygen. The part of the URI after the # sign is called a fragment. The browser doesn't even send it to the web server. It lets a link point to a specific named part of a resource; in HTML pages it links to an element by id.

In contrast, consider this Google Search URI:

 * https://www.google.com/search?q=fish
The ?q=fish is a query part of the URI. This does get sent to the server.
# Hostnames and ports
## Hostnames
A full HTTP or HTTPS URI includes the hostname of the web server, like www.udacity.com or www.un.int. A hostname in a URI can also be an IP address: for instance, if you put http://216.58.194.174/ in your browser, you'll end up at Google. The Internet tells computers apart by their IP addresses; every piece of network traffic on the Internet is labeled with the IP addresses of the sending and receiving computers. Your operating system's network configuration uses the Domain Name Service **(DNS)** — a set of servers maintained by Internet Service Providers **(ISPs)** and other network users — to look up hostnames and get back IP addresses.

Some systems don't have the **host** command, but do have a similar command called **nslookup**. This command also displays the IP address for the hostname you give it; but it also shows the IP address of the DNS server that's giving it the answer.
IP addresses come in two different varieties: the older **IPv4** and the newer **IPv6**.
