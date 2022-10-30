**Wave A Flag on PicoCtf by Ne0exe 30.10.2022**

After downloading I wanted to check out what type of file is it:

`$ file warm 
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=3aa19b2a9cc4e093d64025eab8f510679b523455, with debug_info, not stripped`

ELF 64-bit? What the hell is it? Wikipedia as an antidote:

"In computing, the Executable and Linkable Format[2] (ELF, formerly named Extensible Linking Format), is a common standard file format for executable files, object code, shared libraries, and core dumps."

Executable...hm, let's try running it, but first I need to make it executable with chmod.
`$ sudo chmod +x warm`

`$ ./warm 
Hello user! Pass me a -h to learn what I can do!`

Sure, let's try -h

`$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
`

Oh...thanks, i guess. It was starting to get more interesting. I hope it's not the last one ctf with elf file... and I hope I'm not gonna regret this wish haha Have a nice day!