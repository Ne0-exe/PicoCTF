**Transformation on PicoCtf by Ne0exe 01.11.2022**

Simple stuff, let's check out what do we have:

Chinese text x1
Python ordering script x1
Flags x0

Let's fix it.

`$ cat enc          
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸弰摤捤㤷慽 ` 

Interesting...

According to that script 
`''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
There is a variable called flag. I assume that *enc* is our flag. But it's not gonna work in that case because...well, it's chinese.

`$ file enc 
enc: Unicode text, UTF-8 text, with no line terminators`

I'm not proud of that solution but I just put it into CyberChef and seems like it was UTF-16BE (1201) encoding. I know, obvious thing pff.

I've also tried translating it from chinese (idk why) but it was a dead end.

There you go chef's output:


