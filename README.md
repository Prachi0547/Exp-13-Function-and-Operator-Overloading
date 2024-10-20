# Exp-13-Function-and-Operator-Overloading
# Aim
Write a c++ program:
1. To do function overloading.
2. To do operator overloading.
# Software Used
VS Code and c++ online compiler.
# Theory
In C++, overloading allows developers to define multiple functions or operators with the same name but different behaviors based on their parameters or operands.

Function overloading occurs when multiple functions share the same name but differ in their parameter lists (type, number, or order). The compiler differentiates between these functions based on the arguments passed during a function call.

Operator overloading allows custom types to redefine the way operators work with their objects. This makes user-defined types (like classes) behave more like built-in types.

# Program Code
```
//Function overloading

#include<iostream>
using namespace std;
int add(int a, int b){
    return a+b ;
}
float add(float a, float b)
{
    return a+b;
}
int add(int a, int b , int c){
    return a+b+c;
}
int main() {
    cout<<"Addition of 2 integers: "<<add(3,4)<< endl;
    cout<< "Addition of 2 floats: "<<add(3.5f, 4.5f)<<endl;
    cout<< "Addition of 3 integers: "<< add(1,2,3)<<endl;
    return 0;
    }
```
```
//Operator overloading

#include<iostream>
using namespace std;
class Complex {
    private:
    float real;
    float imag;
     
     public:
     Complex(float r =0 , float i = 0)
     
     {
        real = r;
        imag =i;
     }
Complex operator + (const Complex &obj)
{
    Complex temp;
    temp.real = real + obj.real;
    temp.imag = imag + obj.imag;
    return temp;
}
void display()const {
    cout<< real<<" + "<< imag<< "i"<<endl;
}
};
int main() {
    Complex c1(3.5,2.5);
    Complex c2(1.6,3.7);
    Complex c3 = c1 +c2;
   
    cout << "First complex number: ";
    c1.display();
    cout << "Second complex number: ";
    c2.display();
    cout << "Sum of complex numbers: ";
    c3.display();
    return 0;
}
```

# Output
### Function overloading
![image](https://github.com/user-attachments/assets/b8e8e9ca-e7af-4b9e-943d-e6f06d723e7a)
### Operator overloading
![image](https://github.com/user-attachments/assets/97b3b729-d38d-41d1-8f3a-f8c8cdd23645)

# Conclusion
We learnt how to do function and operator overloading.
