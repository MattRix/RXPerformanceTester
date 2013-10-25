RXPerformanceTester
===================

A simple C# class for comparing the relative performance of different blocks of code.

Usage:

```csharp
RXPerformanceTester.testA = () =>
{
	Math.Sin(0.0);
};

RXPerformanceTester.testB = () =>
{
	Math.Cos(0.0);
};

RXPerfTester.Run(25,10000);
```

You can even do stuff like this: 

```csharp
int[] nums = new int[10000];

RXPerformanceTester.testA = () =>
{
	for(int i = 0; i<nums.Length; i++)
	{
		nums[i] = nums[i];
	}
};

RXPerformanceTester.testB = () =>
{
	int count = nums.Length;
	for(int i = 0; i<count; i++)
	{
		nums[i] = nums[i];
	}
};

RXPerformanceTester.Run(25,100);
```

Enjoy! 
