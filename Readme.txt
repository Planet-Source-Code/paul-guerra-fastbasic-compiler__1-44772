FASTBASIC
By Paul Guerra


Notice: FastBasic is free to use, but if you want to use all or ANY part of it in your own programs and/or languages, you MUST ask me. Otherwise you would be violating the copyright.


What is FastBasic?
¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
FastBasic is a programming language made in Visual Basic 6. It is NOT a scripting language: FastBasic compiles to a p-code that is executed by a runtime (or Virtual Machine, whatever you prefer).
The language itself is very simple. It only handles if's, do's, and things like that, but it can be expanded easily.
Keep in mind that you can't do anything very useful in FastBasic, it is just an educational tool.
Take a look at the examples provided to see some of the things it is capable of doing.


History
¯¯¯¯¯¯¯
I've always liked building programming languages, and this was one of the first I ever did. I created it back in 2001, and has been untouched since then, until now that I decided to make it public. In these two years I learned a lot of compiler theory and I realized that FastBasic doesn't have a future, unless it is totally rewritten from scratch.
Since it's highly possible that I won't update it anymore, I am posting it on PSC because I think it will be useful to some people who want to learn about language creation.


Frequently Asked Question
¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯

Q: The compiler flags the following code as erroneous, but I can't find the error:

Dim Numeric Num
...
If Num=5 Then ...

A: Boolean expressions in FastBasic must be of string-type. One way to solve the problem is this:

Dim Numeric Num
...
If Str(Num)="5" Then ...

-------------------------------------------------------------------


Q: I'm calling a function, but the arguments don't seem to be passed. What's wrong?

A: Unless the call is made from inside an expression, the arguments are ignored, and no error is flaged.

-------------------------------------------------------------------


Q: Can I make recursive modules and functions?

A: Yes, but the variables (and arguments) are global, so you can't have local data.

-------------------------------------------------------------------

Q: In the following code:

If Len(StrVariable)="10" Then ...

the compiler says:

Warning in object Form1.[Load_Form1], line no. 1: Variable undeclared (Len)
Warning in object Form1.[Load_Form1], line no. 1: Assuming 'Len' as string
Error in object Form1.[Load_Form1], line no. 1: Invalid logic operator (()

What is that mean?



A: The compiler found identifier 'Len', which returns an integer value. Since the boolean expression is string, the 'Len' function does not exist. So the compiler warns you about an undeclared variable and assumes it is string. Then the compiler expects to find an operator, but instead finds a parenthesis '('. That is not an operator, and that's the error you see.
Solution:

If Str(Len(StrVariable))="10" Then ...

--------------------------------------------------------------------


If you have more questions, just drop me an e-mail at: pguerra_ar@yahoo.com








This program is provided "as is" without any kind of warranty. I am not responsible of the changes this program could eventually make to your system.

Copyright © 2003 Paul Guerra. All rights reserved.
