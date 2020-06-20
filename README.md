## CrackMeOne - Solution
*Stupid simple* crackme intended for **absolute** beginners. Your task is to find the secret key and enter it in the **password** field.

1. Load crackme in xdbg64
2. Right click -> Search for -> Current Module -> String references
3. Find the line containing the string "Congratulations, you found the secret password".
4. Double click this line.
5. Go back to the crackme, type anything and click Ok. Nothing happens, no bp reached.
6. Put some breakpoints a few lines up, before the jumps.
7. Back to crackme, type anything, click Ok. BP reached.
8. Step over until:


````
mov dl,byte ptr ds:[eax] -- your password
cmp dl,byte ptr ds:[ecx] -- j5%9lk
jne crackmeone...
````

9. Clearly j5%9lk is the right password.
10. Done.

