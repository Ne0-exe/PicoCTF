**Python Wrangling on PicoCtf by Ne0exe 26.10.2022**

After trying to paste the password from pw.txt I get the error: `ValueError: Fernet key must be 32 url-safe base64-encoded bytes. `

I assumed that the password is encrypted using base64. Luckily there's a command called `base64`

`$ base64 pw.txt         
	NjdjNmNjOTY2N2M2Y2M5NjY3YzZjYzk2NjdjNmNjOTYK`

After pasting that value I still got the same error. The thing is this is NOT a 32 bytes, it was about 40, so I executed the previous command one more time but before I created a new file.

`$ echo 'NjdjNmNjOTY2N2M2Y2M5NjY3YzZjYzk2NjdjNmNjOTYK' > new.txt`

`$ base64 -d new.txt
	67c6cc9667c6cc9667c6cc9667c6cc96`

Now let's try pasting it.

`$ python3 ende.py -d flag.txt.en
Please enter the password:67c6cc9667c6cc9667c6cc9667c6cc96
picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}`

Success!