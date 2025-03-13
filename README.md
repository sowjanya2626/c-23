# c-23
Finding the number of vowels,consonants,digits and spaces in a text 
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
	char str[100];
	int v=0,c=0,s=0,d=0,i;
	printf("enter a string:");
	fgets(str,sizeof(str),stdin);
	for(i=0;str[i]!='\0';i++){
		char ch=tolower(str[i]);
		if(ch>='a'&& ch<='z'){
			if(ch=='a'|| ch=='e'|| ch=='i'||ch=='o'||ch=='u')
			   v++;
			else
			   c++;
	    }
	    else if(ch==' '){
	    	s++;
		}else if(isdigit(ch)){
			d++;
		}
    }
    printf("Vowels %d\n",v);
    printf("Consonents %d\n",c);
    printf("Spaces %d\n",s);
    printf("Digits %d\n",d);
    return 0;
}
