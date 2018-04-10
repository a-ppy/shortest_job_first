//# shortest_job_first
//shortest job first
#include<stdio.h>
int main()
{
	int i,n,p[8],min_v,k=1,btime_v=0;
    int bt[10],temp_v,j,at[10],wt[10],tat[10],ta_v=0,sum_v=0;
    float waverage=0,taverage=0,tsum=0,wsum=0;
    printf("\nEnter no. of processes-->");
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
       printf("\tEnter burst time of %d process :",i+1);
       scanf(" %d",&bt[i]);
       printf("\tEnter arrival time of %d process :",i+1);
       scanf(" %d",&at[i]);
    }
    for(i=0;i<n;i++)
    {
     for(j=0;j<n;j++)
       {
         if(at[i]<at[j])
         {
			temp=p[j];
			p[j]=p[i];
			p[i]=temp;
			temp=at[j];
			at[j]=at[i];
			at[i]=temp;
			temp=bt[j];
			bt[j]=bt[i];
			bt[i]=temp;
		 }
		}
	}

}
