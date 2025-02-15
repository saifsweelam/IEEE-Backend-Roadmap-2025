# Entry Level Week 3

## Main Topics

### Networking for Web Developers

- [Arabic Playlist](https://www.youtube.com/playlist?list=PLNE3WjwctlOy1ekMfZl9AbLyFivSgsfml)
- [English Playlist](https://www.youtube.com/playlist?list=PLCy5RQkQgvf4yaL-AMDO8rpAAi90sWfGl)

## Task (30 pts.)

> **Note:** Using proper search methods is allowed as long as you don't copy the answers from ChatGPT or similar tools.

1. Why is studying networking important for web developers? _(1 pts.)_

2. Perform a DNS Lookup for this domain: `https://ieeemansb.org/`. Write the command you used and the IP address you got. _(3 pts.)_

3. Let's play a little game called "TCP or UDP". I will give you a scenario and you have to guess which protocol is being used. _(4 pts.)_

    - You are browsing a website that starts with `https://`.
    - You are sending an email to your friend.
    - Your computer performs a DNS lookup to resolve a domain name to an IP address.
    - You are downloading a file from a server.
    - You are chatting with your friend using a messaging app.
    - You are editing a document on Google Docs and the updates appear instantly on your colleague's device.
    - You are watching a live stream on Twitch.
    - You are playing an online game with your friends.

4. Using an HTTP Client ([like this one](https://reqbin.com/)) send a `GET` request to `https://example.com`, then find the following: _(4 pts.)_
    - The status code of the response.
    - The value of header `Content-Type`.
    - The value of header `Content-Length`.
    - The usage of header `Connection`.

5. Compare between IP address and MAC address in terms of: _(3 pts.)_
    - Structure.
    - Usage.
    - Location in the network layers.

6. How many of the following statements are true? mention them. _(2 pts.)_
    - IPv4 addresses are written in decimal notation separated by periods, while IPv6 addresses are written in hexadecimal notation separated by colons.
    - IPv4 uses 32-bit addresses, while IPv6 uses 128-bit addresses.
    - IPv4 does not support subnetting, while IPv6 supports subnetting.
    - I can conclude my IPv6 address if I know my IPv4 address.

7. Retransmitting the failed transfers and reordering the packets to form the original message is a responsibility of which layer in the OSI model? _(1 pt.)_

8. What is the advantage of the three-way handshake in TCP connection establishment? _(1 pt.)_

9. What is ping? and how does it work? _(2 pt.)_

10. Why do status codes belong to responses and not requests in HTTP? _(2 pts.)_

11. Mention the convenient HTTP response for each of the following scenarios: _(4 pts.)_
    - The client requests a resource that does not exist on the server.
    - The client sends a request that the server cannot understand.
    - The client sends a lot of requests in a short time and the server cannot handle them all.
    - The user enters a wrong password when trying to log in.
    - A user with normal previliges tries to access an admin-only page.
    - The server is under maintenance and cannot handle any requests.
    - The client asks for a page that has been moved permanently to another URL.
    - The client request is handled successfully but there is no content to send back.

12. You're trying to fetch data from a third-party API, but your request times out. Which OSI layers should you check, and how would you troubleshoot the issue? _(3 pts.)_

13. You seem to like games, so let's play another one. I will give you a scenario and you have to guess which OSI layer is responsible for it. _(2 pts.)_
    - A file download is incomplete because some packets were lost in transit.
    - Your web app works fine on `localhost`, but when deployed, it's unreachable due to a misconfigured firewall.
    - Your computer is connected to a Wi-Fi network, but you can't access the internet.
    - You get a 404 error when trying to access a webpage.
    - The browser tells you that the SSL certificate of a website is invalid.
