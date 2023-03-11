### Simple Calculator (30 points, 87 solves)

	Check out my new calculator!(https://simple-calculator.acmcyber.com/)

Let's view the source.

![source](https://s2.loli.net/2023/03/11/yk32GEFbQOqC7He.png)

Flag is in the environment variables. URL seems interesting. `/source?file=app.py`. Is there an Local File Inclusion(LFI)? Let's investigate it.

![path](https://s2.loli.net/2023/03/11/up8SXQ3xm6JYfor.png)

Path traversal doesn't work or there are some filtering behind the scenes. Let's try double `../` .

![lfi](https://s2.loli.net/2023/03/11/yLREShkft4DnaC9.png)

It works. More interestingly, specifying absolute path of the file also would work. For example: `/etc/passwd` but we will read the environment variables, so we can use this example: `/proc/self/environ` . File named "Source" will be downloaded. It contains all of the environment variables, of course with the flag!

![env](https://s2.loli.net/2023/03/11/WEXzOiotS6ZB3YI.png)

	flag{how_do_i_make_my_calculator_work_for_more_inputs}