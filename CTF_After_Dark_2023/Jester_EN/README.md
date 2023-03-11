### Jester (30 points, 58 solves)

```
You are a jester, whose entire life's purpose was to keep the royal family happy and entertained. However, the princess is having some trouble finishing her math homework, and she is about to burst into tears as she stares at the lifeless sheet of paper, as thin as the number of brain cells floating around in her royal brain. If you don't keep her happy, the king and queen can easily chop off your head. Do you think you can save yourself and help keep the royal family from collapsing because of some quick maths(https://jester.acmcyber.com/)?
```

We need to write math solver script in this challenge. Firstly, my final script is not the best and since I'm not in US, my ping was high. In order to solve this challenge, I used asynchronous requests so we can vastly reduce the time per request. You can read more about asynchronous requests and comparison to the requests library [here](https://www.twilio.com/blog/asynchronous-http-requests-in-python-with-aiohttp).

Also, final script doesn't work everytime, but there's a high chance so you can get the flag. Note that the moderators of this ctf said that if you are outside of US or the ping is high, they give you the flag if your script works.

Fortunately, our final script works with a couple of tries. Challenge divided by two parts. In the first part, we were asked simple addition. If you can't do the addition under 1 second, numbers will be changed. Then in the second part, we have to solve the quadratic equation. There are different ways and libraries to solve the quadratic equation. We calculated discriminant and not used any libraries(~except math for calculating the square roots~). [Here](finalscript) is the final script.

	flag{you_ar3_not_a_c1own_you_ar3_th3_3ntir3_circus}