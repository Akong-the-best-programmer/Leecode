1.次方函数pow(x,y)

```c++
int x,y;
pow(x,y);   //x的y次方
```

2.绝对值函数abs()

3.判断一个数是否为2^n

```c++
bool is2N(int dest)
{
	if (dest & (dest - 1)) //核心代码
		return false;
	else
		return true;
}
```

3.判断是否为回文数

```c++
bool isHW(int n){
        int n2=0;
        int temp=n;
        while(temp!=0){
            int x=temp%10;
            n2=n2*10+x;
            temp/=10;
        }
        return n==n2?true:false;
    }
```

4.判断是否为素数

```c++
bool isPrim(int n){
     if(n==1) return false;
     for(int i=2;i*i<=n;i++){
        if(n%i==0) return false;
     }
     return true;
}
```

