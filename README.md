# returning_pointer_funcation_average
2.Write a C program to find the average of the elements of an array .The programe should use a funcation that takes an integer array as input poarameter and returns the average value using a pointer .  


    #include<stdio.h>
    
    float *point(int *arr,int size)
    {
    int i,sum=0;
    for(i=0; i<size; i++)
    {
        sum=sum+*arr;
        arr++;
    }
    float *aver,aver2;
    aver2=(float)sum/size;
    aver=&aver2;
    return aver;

    }

    int main()
    {
    int a[]= {10,20,30,40,50};
    int size=sizeof(a)/sizeof(a[0]);
    float *average=point(a,size);
    printf("%f",*average);


    return 0;
    }

