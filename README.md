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
The path tells the server which resource the client is looking for. 
