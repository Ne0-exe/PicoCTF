**information on PicoCtf by Ne0exe 30.10.2022**

"Files can always be changed in a secret way. Can you find the flag?"

Okay Pico, let's find those changes.

Investigating cat.jpg with file command: 

`$ file cat.jpg 
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3`

Nothing interesting.

I got the feeling that there's something with binary, so let's go with exiftool: 

`$ exiftool cat.jpg`

(...)

License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9

(...)

Oh man, that license reminds me of something, let's see what our chef has to say.

![Screenshot_2022-10-30_02-39-05](https://user-images.githubusercontent.com/64281657/198865985-1aa4d272-28a9-4ec2-b11f-d1251d26b6d7.png)

Yup, yup, intuition did not disappoint me:)
Have a nice day!
