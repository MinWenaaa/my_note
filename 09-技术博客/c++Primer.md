### 4.8.3 指针和字符串
- `std::cout<<`方法传递的是字符串的地址，以减小开销。多数情况下，char数组名、char指针以及用引号阔气的字符串常量都被解释为字符串第一个字符的地址。
- `char[]`与`char*`在输出上没有区别，但`char*`不应该用于输入。
```
ps = new char[strlen(animal) + 1];
ps = animal
```
将修改存储在ps库中的地址，失去程序访问新分配内存的唯一途径。应使用stricpy或strincpy：
```
ps = new char[strlen(animal) + 1];
strcpy(ps, animal);
```
```
char food[20] = "carrots";
strncpy(food, "a panic basket filled with many goodies", 19);
food[19] = '\0';
```
### 4.8.4 自动存储、静态存储和动态存储
1. **自动存储**
函数内部的常规变量，函数调用时自动产生，结束时消亡。存储在栈中。
2. **静态存储**
在函数外定义或使用关键字static。
3. **动态存储**
存储在堆中。允许在一个函数分配内存，在另一个函数中释放。
## 4.9 类型组合
```
#include<iostream>

struct antarctica_years_end {
    int year;
};

int main() {
    antarctica_years_end s01, s02, s03;
    s01.year = 1998;
    antartica_years_end *pa = &s02;
    pa->year = 1999;
    antarctica_years_end trio[3];
    trio[0].yaer = 2003;
    std::cout << trio->year << std::endl;
    const antarctica_years_end **ppa = arp;
    auto ppb = arp;
    std::cout << (*ppa)->year << std::endl;
    std::cout << (*(ppb+1))->year << std::endl;
    return 0;
}
```