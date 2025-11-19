## C++

In C++ main() function is entry point into program. it first execute the main function, what ever function, called inside main function also gets executed in order.

Similar to python 

```python
if name == __main__:
    print("some text")
```

In C++ main function always return a integer number, such as 0 for success, non-zero for failure.

```cpp
int main (void)
{
    return 0;       // 0 means success, program executed succesfully
}

// below code is not accepted, as compiler does not know whether program executed or not.
void main ()
{
    // no return value
}

```

When a program finishes, it sends an exit code to OS. 0 = success. non zero = error occurred. The OS uses this int number to know if program ran correctly.

```cpp 
// cpp

// During function declaration, f we did mention void or didnt mention, it means it does not take any argument. 

// int main(void) = int main()
int main()
{
    return 0;
}

// where as in c, int main(void) = doesnot take arguments, and int main() = can take any argument.
```

## namespace
namespace helps in preventing name conflicts. if for example, we include 2 library, where there is variable called model, program doesnot know which variable to use, and results in error.

```cpp
namespace mynamespace
{
    int value;
    void display()
    {

    }
}
```
To access member of a namespace, use the scope resolution operator ::

```cpp
mynamespace::display();
mynamespace::value = 10;
```

Another use case is to import all variable and functions in namespace globally in program

```cpp
using namespace std;        // permits direct use of cout, cin, endl etc
cout << "Hello, world!";
// it is similar to 
std::cout << "Hello, world!";
```

Nested namespace also exists, such as alpha::beta::x

## pointer

## access specifier

Access Specifier are keywords that controls the visibility and accessibility of class members(variable and methods) to different part of program. Encapsulation.

- public : can be accessed from anywhere, inside and outside of class.
- private : can be accessed from class only. default is private.
- protected : can be accessed from class and by derived (child) class only.

## include

```cpp
#include <Arduino.h>        // searches in system libraries first.

#include "Arduino.h"        // searches in current directory first. useful for our own header files.     
```

