### Secure Platform (15 points, 141 solves)

	Take a look at my super secure website(https://secure-platform.acmcyber.com/). I only let people access the flag I hid there if they're just as secure as I am!

We have a very secure web application. There is one button in this web app and it gives the flag, but there is an error in the /flag page.

![Agent](https://s2.loli.net/2023/03/11/zpYtjx8aPcbXESe.png)

Firstly, I thought we can manipulate the user agent and get the flag, but this is not the point. There is another http header which is called "Sec-CH-UA-Platform" and it was set to "Linux" in my situation. We can use curl and set this header to "INTEGRITY-178B" (I've never heard this operating system before, cool!).

	curl https://secure-platform.acmcyber.com/flag -H 'Sec-CH-UA-Platform: "INTEGRITY-178B"'

![Flag](https://s2.loli.net/2023/03/11/jNkhSmKgs14Vuw3.png)

Unbelievable. Are we a hacker? I think so? Maybe? Anyway, we got the flag and I'm happy. It seems the secure platform is not so secure!

	flag{sh0uldv3_us3d_n4v1g4t0r}

