### Bank (20 points, 92 solves)

	This is a bank. I hate php very much. Here(https://bank.acmcyber.com/login.php)

We have a login page.

![Tables](https://s2.loli.net/2023/03/11/j81gcRGs3o7YLwu.png)

We have an information about columns and tables. This is the sign of SQL Injection. Now let's do some enumeration. Single quote is perfectly fine to test if there is an sql injection. 

![Result](https://s2.loli.net/2023/03/11/LsUx28yRaBhMWeq.png)

We got an error. Also we have the query, unfortunately we don't have any results(for now). Continuing our enumeration.

![orderby3](https://s2.loli.net/2023/03/11/g5LR7njiE8CsGXK.png)

That's interesting. I was expecting to get an error again since we know there are 2 columns in the "flags" table. I used hashtag as commenting the rest of the line. Double dash didn't work for some reason. Let's try ORDER BY 4

![orderby4](https://s2.loli.net/2023/03/11/NkzH4vf56yCVJlu.png)

Now we get an error. So, there is a third column plus flag and value columns. We can use `' UNION SELECT flag, value, null FROM flags#` to get all values from the "flags" table.

![query](https://s2.loli.net/2023/03/11/7exyY28h1MQzip6.png)

Interestingly, SELECT in our query seems to be disappeared. There should be a filter. I assume that filter replaces SELECT query with an empty string. Therefore, we need to use `SELSELECTECT` instead of `SELECT`. Did you see the difference? If the application replaces SELECT with an empty string, SELSELECTECT **becomes** `SELECT`. Cool! Let's try this.

Nice! We got the flag and lessons learned: basic filtering can be easily bypassed.

![flag 7](https://s2.loli.net/2023/03/11/gTSuRIUeNdQkxGZ.png)

	Exploit: ' UNION SELSELECTECT flag,value,null FROM flags#
	flag{3min3m_kind@_wa$hed}