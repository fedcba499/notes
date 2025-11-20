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

pointer stores memory address of variable
```cpp
int *age = 10;          // pointer is decalred using astrisk *
```

## reference

reference is used for **alias**, we need to create another name for variable reference is used.

```cpp
int x = 10
int &ref = x    // & is used to declare reference
```

## access specifier

Access Specifier are keywords that controls the visibility and accessibility of class members(variable and methods) to different part of program. ```Encapsulation```.
- **public** : can be accessed from anywhere, inside and outside of class.
- **private** : can be accessed from class only. default is private.
- **protected** : can be accessed from class and by derived (child) class only.

## include

```cpp
#include <Arduino.h>        // searches in system libraries first.

#include "Arduino.h"        // searches in current directory first. useful for our own header files.     
```

## Data Types

Exact Width Integer Type

```cpp
int8_t    // signed, 8 bits  (-128 to 127)
uint8_t   // unsigned, 8 bits (0 to 255)

int16_t   // signed, 16 bits (-32,768 to 32,767)
uint16_t  // unsigned, 16 bits (0 to 65,535)

int32_t   // signed, 32 bits
uint32_t  // unsigned, 32 bits

int64_t   // signed, 64 bits
uint64_t  // unsigned, 64 bits
```

## struct
struct is short for structure. It is grouping of several data types and functions. It is similar to class, but with default access as **Public**. Struct can be used as an array with various datatypes. 

```cpp
struct myStruct()
{
    int age = 10;
    string name = kumar;

    void getName()
    {
        cout << name;
    }
}

// initiate 
myStruct student;

cout << student.age;
```

## enum
enum is short for enumeration (make a list of / enumerate). It is assigning Interger name. It improves code readability.

```cpp
enum dayOfWeek() 
{
    MONDAY,
    TUESDAY, 
    WEDNESDAY,
    THURSDAY, 
    FRIDAY,
    SATURDAY,
    SUNDAY
}

// if i print monday it will show as int 0
cout<< dayOfWeek::MONDAY        // 0
```

We can relate to Arduino constants like

```cpp
enum value()
{
    LOW,                // 0
    HIGH                //1
}

enum mode()
{
    INPUT,              // 0
    OUTPUT,             // 1
    INPUT_PULLUP        // 2
}
```

## typedef

typedef is used for alias. 

> similar to **as** in python

```cpp
typedef unsigned long ulong
typedef unsigned int uint
```

## define
define is used for **alias**, but direct text replacement only without type safety.

## Singleton Pattern

Singleton meaning "There can be only one". It ensures only one object / Instance of a class exists in entire program.

In all Microelectronics ther can be only one
- Wire (I2C) Bus
- SPI
- SD card

Only One can exists. so it be better to have Single ton Class.

## Factory Pattern
Factory Pattern is a Design Pattern (Like Singleton Pattern) where we have a special "factory" / class that creates objects for us, instead of using constructors directly.

```cpp
// without factory / seperate class - direct construction

TinyGPSPlus gps;        

// we call constructor method of TinyGPSPlus class, it creates object of TinyGPSPlus Class.

// With factory - function creates it

File myFile = SD.open("test.txt")       

// SD.open() function create a object or instance of File class for us.
```     

File Class constructor method is Private, it can be accessed by SD.open() function.

> Used when it requires complex object creation, need validation.

## Wrapper/ Facade Pattern
Simple interface for complex system. 

Ex : SPI.h is low level library, designed for dealing with Serial Peripheral Communicaiton. It is difficult to use SPI.h, so SD.h class is created to simplify certain SPI.h tasks releated to SD card Handling, like open file, read file , write to file etc.

SD class acts as Wrapper or Facade to Simplify usage of SPI class.



