#include <stdio.h>

struct student
{
char name[10],group[10];
int rollno;
float s1,s2,s3,total,avg;
};
void main ( )
{
static struct student s[100];
int n,i,j;
printf("Enter the number of Students: ");
scanf("%d",&n);
for(i=0; i<n; i++)
{
        printf("Enter  rno: ");
        scanf("%d", &s[i].rollno);
        printf("Enter  name: ");
        scanf("%s", s[i].name);
        printf("Enter  group: ");
        scanf("%s", s[i].group);
        printf("Enter s1,s2,s3: ");
        scanf("%f%f%f", &s[i].s1,&s[i].s2,&s[i].s3);
        printf("rno:%d,name:%s,group:%s,s1:%f,s2:%f,s3:%f\n",s[i].rollno,s[i].name,s[i].group,s[i].s1,s[i].s2,s[i].s3);
        s[i].total=s[i].s1+s[i].s2+s[i].s3;
        printf("total is%f\n",s[i].total);
        s[i].avg=s[i].total/3;
        printf("average is:%f\n",s[i].avg);
        if(s[i].s1>=35&&s[i].s2>=35&&s[i].s3>=35)
        {
            printf("Result is:PASS");
                    }
        else
        {
            printf("Result is:FAIL");
        }
        }
    }
