在看[Solving problem with C++](https://www.pearson.com/us/higher-education/program/PGM1743309.html)~~中文版~~看到class一节时候，介绍过成员的两种形式：
```cpp
class ExampleClass
{
    public:
        char PublicMember;
    private:
        char PrivateMember;
}
```
但是在继承方式一节中，~~一不小心~~STFW发现了原来还有第三种形式`protected`.但是似乎对于`protected`与`private`的区别介绍得不多。继续STFW，得到了如下解释：

>Private members are only accessible within the class defining them.
>Protected members are accessible in the class that defines them and in classes that inherit from that class.
>Edit: Both are also accessible by friends of their class, and in the case of protected members, by friends of their derived classes.

(Source: [StackOverflow](https://stackoverflow.com/questions/224966/what-is-the-difference-between-private-and-protected-members-of-c-classes))

在[isocpp](https://isocpp.org/wiki/faq/basics-of-inheritance)中的解读：

>What’s the difference between public, private, and protected?  
A member (either data member or member function) declared in a private section of a class can only be accessed by member functions and friends of that class
A member (either data member or member function) declared in a protected section of a class can only be accessed by member functions and friends of that class, and by member functions and friends of derived classes
A member (either data member or member function) declared in a public section of a class can be accessed by anyone

遂实验求证：(`./testcode.cpp`)
