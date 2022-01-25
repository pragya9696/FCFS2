# FCFS2

PRACTICE
CERTIFICATIONNEW
COMPETE
LEADERBOARD
Search
1
 pragya_2024cse11 
All Contests  24-28thJan  FCFS (First Come First Serve) CPU Scheduling Algorithm with different Arrival Time
FCFS (First Come First Serve) CPU Scheduling Algorithm with different Arrival Time
Problem
Submissions
Leaderboard
Discussions
Submitted 5 minutes ago • Score: 50.00Status: Accepted
 Test Case #0
 Test Case #1

Submitted Code
Language: C

 Open in editor
1
#include <stdio.h>
2
#include <string.h>
3
#include <math.h>
4
#include <stdlib.h>
5
​
6
int main() {
7
    int i,j,temp,p[4],a[4],b[4],w[4],sum=0;
8
    for(i=0;i<4;i++)
9
        scanf("%d%d%d",&p[i],&a[i],&b[i]);
10
    for(i=0;i<4;i++)
11
    {
12
        for(j=i+1;j<4;j++)
13
        {
14
        if(a[i]>a[j])
15
        {
16
            temp=a[i];
17
            a[i]=a[j];
18
            a[j]=temp;
19
            temp=b[i];
20
            b[i]=b[j];
21
            b[j]=temp;
22
            temp=p[i];
23
            p[i]=p[j];
24
            p[j]=temp;
25
            
26
        }
27
    }
28
    }
29
  
30
    for(int i=0;i<4;i++)
31
    {
32
        if(i==0)
33
        w[i]=0;
34
        else
35
        {
36
            sum=sum+b[i-1];
37
            w[i]=sum-a[i];
38
        
39
        }
40
    }
41
    for(int i=0;i<4;i++)
42
    {
43
        for(int j=0;j<4-1-i;j++)
44
        {
45
            if(p[j]>p[j+1])
46
            {
47
                int temp=p[j];
48
                p[j]=p[j+1];
49
                p[j+1]=temp;
50
                int temp1=w[j];
51
                w[j]=w[j+1];
52
                w[j+1]=temp1;
53
            }
54
        }
55
    }
56
    for(int i=0;i<4;i++)
57
    {
58
        if(i==3)
59
            printf("P%d (WT=%d)",p[i],w[i]);
60
        else
61
            printf("P%d (WT=%d), ",p[i],w[i]);
62
    }
63
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
64
    return 0;
65
}
66

