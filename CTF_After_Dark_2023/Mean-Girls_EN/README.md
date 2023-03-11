### Mean Girls (10 points, 259 solves)

	Get in loser, we're going shopping. But only if you're fetch enough! (https://lness02.github.io/meangirls/)

![Mean Girls](https://s2.loli.net/2023/03/11/s2XTGVElQy6cLto.png)

This challenge has a login page and we need to hack(wow!). Let's view the source code. 

![Source_code](https://s2.loli.net/2023/03/11/URClzEtnJFg4XN3.png)

There are two findings in there. One of it is login-page.css and login-page.js. Let's take a look at js. 

![Creds](https://s2.loli.net/2023/03/11/JH7W2YPBxfv9gch.png)

Boom! We have credentials! But after we logged in. There are no flag or anything suspicious. Let's view the source again logging in.

![Flaggy](https://s2.loli.net/2023/03/11/WyHheRSYxnatM3N.png)

Yay! We got the fla-...? What the heck is this? It is not the flag! Now I understand. They're talking about the caesar cipher! Now there are bunch of different websites to decrypt caesar. We will be using cyberchef.

![Flag 4](https://s2.loli.net/2023/03/11/kQuBUn4scRPMtdw.png)

We got the flag! Rotating 23 times was enough. So, that means if we shift all the characters to left 3 times, we can get our flag! (You can try! It's like magic!) Another 10 points comes to our team!

	flag{on_w3dn3sd4ys_w3_we4r_p1nk}