### Challenge 5 - Star Poet Blog (10 points, 119 solves)

	oh dear... someone finding my password.txt i could not bear... but no fear... encrypted it i did to make it unclear... (*note: flag is all lowercase). Visit (https://star-poet-blog.acmcyber.com/)

![Poetry](https://s2.loli.net/2023/03/11/gl4zmvnyeOEwVWp.png)

There are two pages with an HTML extensions. The First one is about me and the second one is poetry 101. About me page introduces Edgar Allan Poe to us. Poetry 101 is shown below.

![Poem](https://s2.loli.net/2023/03/11/dZQ6mN5gehBz4sF.png)

It tells us what is a poem. Nothing interesting (No offense, I like poetry).

All of the poems in the first image is a txt file. This is the first poem's url:
	https://star-poet-blog.acmcyber.com/archive/annabel_lee.txt

If you read the challenge carefully, password.txt mentioned. Let's navigate to `https://star-poet-blog.acmcyber.com/archive/password.txt`

![Flaggy 2](https://s2.loli.net/2023/03/11/CuSVaGB8demWfIX.png)

A-ha! We got the flag or I thought we got it. Answer is the second one. I can say that I thought 2 days for this challenge and tried the online tools to decipher this "book cipher". I've never read the poetry 101 page again. So finally, I read it again, then I took another look at the digits which are in the flag. I got it. Each of the 4-digit numbers have this order: 1st digit is the number of poem which is provided in home page. 2nd digit is the stanza inside the poem. 3rd one is the line inside that stanza. 4th digit is the word inside that line.

Here is an example for the first 4-digit number, 1377. We read the 1st poem which is the "Annabel Lee". Then we choose 3rd stanza. 

![](https://s2.loli.net/2023/03/11/7etBsCmfoW4vplJ.png)

Then we choose the 7rd line in the stanza, and the 7rd word in that line is our first word inside the flag.

I repeated this whole process for 5 times and we got the flag!

	flag{sepulchre_tombstone_spirit_grains_nevermore}