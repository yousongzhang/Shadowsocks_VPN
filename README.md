# Shadowsocks_VPN

# purpose

1. deploy Shadowsocks VPN Sever - Jigsaw outline
2. use WireShark to catch packets between VPN server and client. study how chacha20-ietf-poly1305 encrypt/decrypt package.


# background knowledge 

## What Is Shadowsocks?
An open-source SOCKS5-based proxy project, Shadowsocks is an intermediary that is mainly **designed around bypassing censorship**. It was first released in 2012 by its creator, a Chinese programmer under the pseudonym “clowwindy”.

In 2015, the programmer announced that they were retiring from the project due to being contacted by police. Since then, Shadowsocks has been developed and maintained by numerous collaborators.

## Shadowsocks vs VPN
There is one major similarity between VPN and Shadowsocks — their ability to connect you to certain websites that are normally off-limits due to government censorship, geoblocks, or otherwise.

Given its original objective of bypassing the Great Firewall of China, **Shadowsocks focuses on circumventing traffic restrictions**. It utilizes HTTPS, thus disguising traffic so that it can move past the censorship measures in place.

Unlike VPN, Shadowsocks **isn’t designed for privacy and anonymity**. While VPN encrypts all traffic as long as it is enabled, the packages in Shadowsocks are “blank” — that is, they are unencrypted. The main idea behind this is to make your data look more like HTTPS traffic, so that it can move around unrestricted.

Due to its use of SOCKS5 proxies, Shadowsocks **doesn’t send all your traffic through a server, as opposed to VPN**. And in contrast to traditional ssh SOCKS5 proxies, Shadowsocks works with multiple TCP connections. The result is much faster speeds compared to the alternatives.

## Benefits of Shadowsocks
The biggest advantage of Shadowsocks is its easy setup. The technology is a simple and capable proxy that doesn’t take long to setup and is perfect for accessing restricted content.

Another benefit of Shadowsocks is its selective disguising of traffic. **You can choose which part of your traffic is affected** by Shadowsocks — this makes it possible to access restricted content both inside and outside of your location.

Take the following scenario for example: you are in China and you want to access Gmail. By using Shadowsocks, you can choose the Gmail traffic to be “camouflaged”, thus bypassing the Chinese government’s block.

However, you will still be able to access the China-only websites. By contrast, a VPN would encrypt all traffic to your chosen server, thus making China-exclusive sites unavailable on the same device.

Last but not least, Shadowsocks is **very difficult — if not impossible — to detect and block**. The masking of traffic to make it appear as HTTPS is the main reason for that.

On the other hand, VPN’s modus operandi and its immense popularity have made it easier for governments and platforms to block the technology or force major corporations to remove VPN products from their stores (Apple removing VPN apps from the Chinese App Store is an example).



## Installation
Step1: 

Go to Jigsaw outline's website: https://getoutline.org  use chrome browser and download outline.

Step2: Install and Manage Shadowsocks Server 

A:install outline manager and install docker on ubuntu system.

B: Create a client access key through outline manager.
![Alt text](https://getoutline.org/modern/img/manager-download-2x.png)

Step3: 

Download shadowsocks client and input access key, start VPN connction with server.




# Reference

1. Jigsaw outline:  google support VPN open souce project   
https://github.com/Jigsaw-Code

2. Shadowsocks: an open-source encrypted proxy project(server + client). it becomes popular in China after SSH tunnel blocked by The Great Firewall of China. it can proxy UDP traffic.   
https://en.wikipedia.org/wiki/Shadowsocks

3.  chacha20-ietf-poly1305 : encrypt/decrypt Protocal  
https://tools.ietf.org/html/rfc7539  
https://en.wikipedia.org/wiki/Poly1305

4. SOCKS Protocol
https://tools.ietf.org/html/rfc1928#section-5 


