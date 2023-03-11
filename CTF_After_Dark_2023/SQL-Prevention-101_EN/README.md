### SQL Prevention-101 (20 points, 132 solves)

	Just try to hack my login(https://sql-prevention-101.acmcyber.com/) with account "admin", I've taken all the precautions that I can...

![sqlprevent](https://s2.loli.net/2023/03/11/LJCvKAFtkcip4bG.png)

Let's try `admin'--` as username and `a` as password.

![doubledash](https://s2.loli.net/2023/03/11/9NpkC8aFGqdjz2Q.png)

We get an error. Cool! Then we can use `#` (hashtag). It's the same thing, comments rest of the line. Exploit:

	username: admin'#
	password: a

![flag 10](https://s2.loli.net/2023/03/11/ygMa1IEvSBop9zh.png)

Someone forgot to filter hashtag!

	flag{curse_you_mysql!}