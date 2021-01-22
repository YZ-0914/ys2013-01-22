# ys2013-01-22
#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<string.h>
////1.写一个函数可以判断一个数是不是素数。
//void sushu(int i, int j)
//{
//	for (j = 2; j < i; j++)
//		if (i%j == 0)
//		{
//		printf("这个数不是素数");
//		}
//		else
//		{
//			printf("这个数是素数");
//		}
//}
//int main()
//{
//	int i = 0;
//	int j = 0;
//	scanf("%d\n", &i);
//	sushu(i,j);
//	return 0;
//}this is by me,that is fault.

////是素数返回1，不是素数返回0
//int is_prime(int n)
//{
//	//2-->n-1
//	int j = 0;
//	for (j = 2; j < n; j++)
//	{
//		if (n%j == 0)
//			return 0;
//	}
//	return 1;
//}
//int main()
//{
//	//打印100-200之间的素数
//	int i = 0;
//	for (i = 100; 1 <= 200; i++)
//
//	{
//		//判断i是否为素数
//		if (is_prime(i) == 1)
//			printf("%d", i);
//	}
//	return 0;
//}

//int sushu(int i, int j)
//{
//	for (j = 2; j < i; j++)
//		if (i%j == 0)
//		{
//		return 0;
//		}
//		else
//		{
//			return 1;
//		}
//}
//int main()
//{
//	int i = 0;
//	int j = 0;
//	for (i = 100; i <= 200; i++)
//	{
//		if (sushu(i,j) == 1)
//			printf("%d", i);
//	}
//	return 0;
//}

#include<math.h>
//int is_prime(int n)
//{
//	int j = 0;
//	for (j = 2; j <=sqrt(n*1.0); j++)
//	{
//		if (n%j == 0)
//			return 0;
//	}
//	return 1;
//}
//int main()
//{
//	int i = 0;
//	for (i = 100; i<= 200; i++)
//	{
//		if (is_prime(i) == 1)
//			printf("%d", i);
//	}
//	return 0;
//}

////3.写一个函数，实现一个整形有序数组的二分查找。
////                  本质上arr是一个指针
//int binary_search(int arr[], int k,int sz)
//{
//	//算法的实现
//	//int sz = sizeof(arr) / sizeof(arr[0]);
//	int left = 0;
//	int right = sz - 1;
//	while (left<=right)
//	{
//		int mid = (left + right) / 2;//中间元素的下标
//		if (arr[mid] < k)
//		{
//			left = mid + 1;
//		}
//		else if (arr[mid]>k)
//		{
//			right = mid - 1;
//		}
//		else
//		{
//			return mid;
//		}
//	}
//	return -1;
//}
//int main()
//{
//	//二分查找
//	//在一个有序数组中查找具体的某个数
//	//如果找到了返回，这个数的下标。找不到的返回-
//	int arr[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
//	int k = 7;
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	//                    传递过去的是数组arr首元素的地址
//	int ret= binary_search(arr, k,sz);
//	if (ret == -1)
//	{
//		printf("找不到指定的数字\n");
//	}
//	else
//	{
//		printf("找到了，下标是%d\n",ret);
//	}
//	return 0;
//}

////4.写一个函数，每调用一次这个函数，就会将num的值增加1。
//void Add(int* p)
//{
//	(*p)++;
//}
//int main()
//{
//	int num = 0;
//	//调用函数，使得num每次增加1
//	Add(&num);
//	printf("num=%d\n", num);//1
//	Add(&num);
//	printf("num=%d\n", num);//2
//	Add(&num);
//	printf("num=%d\n", num);//3
//	return 0;
//}

////函数的嵌套调用
//void new_line()
//{
//	printf("hehe\n");
//}
//void three_line()
//{
//	int i = 0;
//	for (i = 0; i < 3; i++)
//	{
//		new_line();
//	}
//}
//int main()
//{
//	three_line();
//	return 0;
//}

////链式访问
//int main()
//{
//	int len = 0;
//	//1
//	len = strlen("abc");
//	printf("%d\n", len);
//	//2
//	printf("%d\n", strlen("abc"));
//}

//int main()
//{
//	printf("%d", printf("%d", printf("%d", 43)));//43
//	//printf打印字符个数
//	//printf("%d", printf("%d", 2));
//	//printf("%d", 1);
//	return 0;//43 2 1
//}//4321

//int main()
//{
//	printf("%d\n", printf("%d\n", printf("%d\n", 43)));
//	return 0;//43 3 2
//}

////声明函数
//int Add(int, int);
//
//int main()
//{
//	int a = 10;
//	int b = 20;
//	int sum = 0;
//	//调用函数
//	sum = Add(a, b);
//	printf("%d\n", sum);
//	return 0;
//}
////函数的定义
//int Add(int x, int y)
//{
//	int z = x + y;
//	return z;
//}//函数放后面要在前面声明

//#ifndef __ADD_H__
//#define __ADD_H__
////函数的声明
//int Add(int x, int y);
//#endif

////最简单的递归
//int main()
//{
//	printf("hehe");
//	main();
//	return 0;
//}

////练习1：（画图讲解）接受一个整型值（无符号），按照顺序打印它的每一位。例如：输入：1234，输出 1 2 3 4.
//void print(int n)
//{
//	if (n > 9)
//	{
//		print(n / 10);
//	}
//	printf("%d ", n % 10);
//}
//int main()
//{
//	unsigned int num = 0;
//	scanf("%d", &num);//1234
//	//递归
//	print(num);
//	//print(1234)
//	//print(123)4
//	//print(12)34
//	//print(1)234
//	return 0;
//}

//int my_strlen(char* str)
//{
//	int count = 0;
//	while (*str != '\0')
//	{
//		count++;
//		str++;
//	}
//	return count;
//}
//int main()
//{
//	char arr[] = "bit";
//	//int len = strlen(arr);//求字符串长度
//	//printf("%d\n", len);
//	//模拟实现了一个strlen函数
//	int len = my_strlen(arr);//arr是数组，数组传参，传过去的不是整个数组，而是第一个元素的地址。
//	printf("len=%d\n", len);
//	return 0;
//}

//递归的方法
int my_strlen(char* str)
{
	if (*str != '\0')
		return 1 + my_strlen(str + 1);
	else
		return 0;
}
//把大事化小
//my_strlen("bit");
//1+my_strlen("it");
//1+1+my_strlen("t")
//1+1+1+my_strlen("")
//1+1+1+0
//3
int main()
{
	char arr[] = "bit";
	//int len = strlen(arr);//求字符串长度
	//printf("%d\n", len);
	//模拟实现了一个strlen函数
	int len = my_strlen(arr);//arr是数组，数组传参，传过去的不是整个数组，而是第一个元素的地址。
	printf("len=%d\n", len);
	return 0;
}
