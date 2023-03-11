### What's on the Menu? (20 points, 102 solves)

	You're invited to Hawthorne, the restaurant of world famous chef, Julian Slowik. Try to order something on _the Menu_. Visit (https://whats-on-the-menu.acmcyber.com/).

We have a cool restaurant here. Let's view the source.

![Restaurant](https://s2.loli.net/2023/03/11/RLihBeNzI16P24o.png)

Oh no! We can see the menu only if we send the post request! This time we will use small instead of using curl. 

```
import requests
url = "https://whats-on-the-menu.acmcyber.com"
r = requests.post(url)
print(r.text)
```

![Response](https://s2.loli.net/2023/03/11/c9lw86pHTQI5rYM.png)

Now we have to use MenuBrowser. We can manipulate the User-Agent header.

```
import requests
url = "https://whats-on-the-menu.acmcyber.com"
useragent={"User-Agent":"MenuBrowser"}
r = requests.post(url, headers=useragent)
print(r.text)
```

![Referer](https://s2.loli.net/2023/03/11/zABUD6bIc5JYe3h.png)

That's another request. We can use "Referer" header and get our flag! You can see the [final script here](script.py).

![flag 11](https://s2.loli.net/2023/03/11/5A7jQcl3VtTNawq.png)

	flag{jUs1_8_pLa1n_c3e5eBur9eR}