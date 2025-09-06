# Identifier Validation using LEX

## 📌 Description
This program is a **LEX program** that checks whether a given input string is a **valid identifier**.  

An identifier is considered valid if:
- It starts with a **letter (a–z or A–Z)**  
- It can be followed by **letters or digits (0–9)**  

Examples of valid identifiers:  
heloo,x,x1,abc123

Examples of invalid identifiers:  
123abc, @var, abc-12

**write a lex program to  identify the valid  identifier?**
%{
#include<stdio.h>
%}

letter  [a-zA-Z]
digit   [0-9]

%%
{letter}({letter}|{digit})*  {printf("%s is an identifier\n",yytext);}
%%

int main()
{
yylex();
return 0;
}

**how to Compile & Run**

Save the program as gedit identifier.l(or)nano identifier.l

Run the following commands:

lex identifier.l
cc lex.yy.c -ll (or)gcc lex.yy.c -o identifier
./a.out(or)./identifier


Enter test inputs :

abc123
1abc
x

📊 Sample Output
Text Output
abc123 is an identifier
x is an identifier


(No output for 1abc since it is invalid)

✅ Conclusion

This Lex program helps to validate identifiers based on rules used in programming languages (like C).
It ensures identifiers always start with a letter and may contain letters and digits afterwards.

