# Identifier1.lexprogram
write a lex program to  identify the valid  identifier?
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


