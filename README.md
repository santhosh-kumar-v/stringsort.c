#include<stdio.h>
#include<string.h>

int main() {
int i,j,n;
scanf("%d",&n);
char s[n][100],t[100];
for(i=0;i<n;i++)
{
    scanf("%s",s[i]);
}
for(i=0;i<n;i++)
{
    for(j=i+1;j<n;j++)
    {
        if((strlen(s[i])>strlen(s[j]))||(strlen(s[i])==strlen(s[j])&&strcmp(s[i],s[j])>0))
        {
            strcpy(t,s[i]);
            strcpy(s[i],s[j]);
            strcpy(s[j],t);
        }
    }
}
for(i=0;i<n;i++)
{
    printf("%s ",s[i]);
}
}
