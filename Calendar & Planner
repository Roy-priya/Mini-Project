#include<stdio.h>
#include <stdlib.h>

int GetFirstDayOfTheYear(int year)
{
    int day= (year*365 + ((year-1) / 4) - ((year-1) / 100) + ((year-1) / 400)) % 7;
    return day;
}

int main()

{
    char *months[]={"January","February","March","April","May","June","July","August","September","October","November","December"};
    int DaysInMonth[]={31,28,31,30,31,30,31,30,31,30,31,30};
    int i,j,totaldays,weekday=0,spacecounter=0,year;
    printf("enter the year\n");
    scanf("%d",&year);

    //check if it is leap year or not
    if(year%4==0&&year%100!=0||year%400==0)
    {
        DaysInMonth[1]=29;
    }

    //get the first day of the year
    weekday=GetFirstDayOfTheYear(year);
    for(i=0;i<12;i++)
    {
        printf("\n\n             %s                \n",months[i]);
        printf("\n  Sun  Mon  Tue  Wed  Thu  Fri  Sat  \n\n");
        for(spacecounter=1;spacecounter<=weekday;spacecounter++)
        {
            printf("     ");
        }
        totaldays=DaysInMonth[i];
        for(j=1;j<=totaldays;j++)
        {
             printf("%5d",j);
             weekday++;
             if(weekday>6)
             {
                weekday=0;
                printf("\n");
             }
        }

    }

    FILE *fp;
    struct planner{
        int pdate;
        char pmonth[15];
        char ptime[15];
        char pplan[100];
    };
    fp=fopen("planner3.txt","a+");
    if(fp==NULL){
        printf("file not created.");
        exit(1);
    }
    printf("\nfile created\n ");
    struct planner plan[100];
    int flag=0,x=0;
    
        
            for(x=0;x<100;x++){
                if(flag==0){
                        fflush(stdin);
                        printf("enter the date you are planning for something:\n");
                        scanf("%d%s",&plan[x].pdate,&plan[x].pmonth);
                        fprintf(fp,"\n\n%d %s %d",plan[x].pdate,plan[x].pmonth,year);
                        fflush(stdin);
                        printf("Enter your time:\n");
                        scanf("%s",&plan[x].ptime);
                        fprintf(fp,"\n%s",plan[x].ptime);
                        printf("enter your plan:\n");
                        
                        fflush(stdin);
                        scanf("%[^\n]s",&plan[x].pplan);
                        
                        fprintf(fp,"\t %s",&plan[x].pplan);
                        fflush(stdin);
                        printf("enter 0 to continue planning your schedule and 1 to exit:");
                        scanf("%d",&flag);


                }
                else if(flag==1)
                    break;
                
                
                


            }
            printf("\nAll the plans are:\n\nDate:\t");
            
            
            fclose(fp);
            int b;
             printf("All the plans are:\n\n");
            for(b=0;b<x;b++){
       
             printf("Date: %d %s %d\n Time:%s\n Plan:%s\n\n",plan[b].pdate,plan[b].pmonth,year,plan[b].ptime,plan[b].pplan);
            }
            return 0;



}

   
