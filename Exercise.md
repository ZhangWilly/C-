######Exercise1(4月10號)

參考老師上課內容

================================================================

#include <iostream>
	
using namespace std;

int main()

{

  const int NUMBER_OF_ELEMENTS = 5; //平均值的元素數量
  
  double numbers[NUMBER_OF_ELEMENTS];
  
  double sum = 0;

  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
  
  {
  
   cout << "Enter a new number: ";
    
   cin >> numbers[i];
   
   sum += numbers[i];
   
  }

  double average = sum / NUMBER_OF_ELEMENTS;

  int count = 0; // 這邊是要找高於平均值的數字數量
  
  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
  
   if (numbers[i] > average)
    
   count++;

  cout << "Average is " << average << endl;
  
  cout << "Number of elements above the average " << count << endl;
  
  system("pause");
  
  return 0;
  
}

平均數字跟高於平均值數量的程式碼

================================================================

######Exercise2(4月10號)

參考老師上課的內容

================================================================

#include <iostream>

using namespace std;

int main()

{
  const int NUMBER_OF_ELEMENTS = 5;
  
  double numbers[NUMBER_OF_ELEMENTS];
  
  double sum = 0;

  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
  
  {
  
   cout << "Enter a new number: ";
    
   cin >> numbers[i];
    
   sum += numbers[i];
    
  }

  double average = sum / NUMBER_OF_ELEMENTS;

  int count = 0; // The number of elements above average
  
  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
  
   if (numbers[i] > average)
    
   count++;

  cout << "Average is " << average << endl;
  
  cout << "Number of elements above the average " << count << endl;
  
  system("pause");
  
  return 0;
  
}

平均數字跟高於平均值數量還有加上平方過後的平均數字跟高於平方平均後數字的數量的程式碼

================================================================

######Exercise3(4月17號)

參考老師上課的內容

================================================================

#include <iostream>
	
using namespace std;

int main()

{

int math,matha[10];

for(math=0;math<10;math++)

matha[math]=math;

for(math=0;math<10;math++)
	
cout << matha[math] << endl;
		
return 0;
    
用迴圈把數字存入matha陣列中並印出

================================================================

######Exercise4(4月17號)

參考老師上課的內容

================================================================

#include <iostream>
	
#include <iomanip>
	
using namespace std;

int fun(int array[3][3])

{

int i,j,t;
	
for(i=0;i<3;i++)
	
for(j=0;j<i;j++)
		
{

t=array[i][j];
	
array[i][j]=array[j][i];
	
array[j][i]=t;
	
}

return 0;

}

int main()

{

int i,j;
	
int array[3][3]={{1,2,3},{4,5,6},{7,8,9}};
	
cout << "Converted Front" <<endl;
	
for(i=0;i<3;i++)
	
{
	
for(j=0;j<3;j++)

cout << setw(7) << array[i][j] ;

cout<< endl;

}
	
fun(array);

cout << "Converted result" <<endl;

for(i=0;i<3;i++)

{

for(j=0;j<3;j++)

cout << setw(7) << array[i][j] ;

cout<< endl;

}

   return 0;
   
}

先印出陣列123456789,利用副函式 產生對角交換的功用

================================================================

######Exercise5(4月17號)

參考老師上課的內容

================================================================

#include<iostream>
	
using namespace std;

int main()

{

int i;

char array[12];

array[0]='a';

array[1]='b';

array[2]='b';

printf("%s\n",array);

  return 0;
    
}

字元陣列存了3個分別為abb後面宣告，輸出後只會顯示"abb"。

================================================================

######Exercise6(4月17號)

參考老師上課的內容

================================================================

#include<iostream>
	
using namespace std;

int main()

{

int i;
	
char array[12]={'H','E','L','L','O',' ','W','O','R','L','D'};
	
for(i=0;i<12;i++)
	
cout<<array[i];
		
cout << endl;
	
   return 0;
   
}

在原先的字元陣列裡面放入HELLO WORLD，並用迴圈把陣列裡的字元一個字元一個字元的輸出。

================================================================

######Exercise7(4月17號)

參考老師上課的內容

================================================================

#include<iostream>
	
#include<string>
	
using namespace std;

int main()

{

char str1[30],str2[20];
	
cout<<"please input string1:"<< endl;
	
gets(str1);
	
cout<<"please input string2:"<<endl;
	
gets(str2);
	
//	strcat(str1,str2);

cout <<"Now the string1 is:"<<endl;
	
puts(str1);
	
   return 0;
   
}

要求使用者輸入兩次字串，結果再顯示一次第一個字串。

================================================================

######Exercise8(5月1號)

參考老師上課的內容

================================================================

#include<iostream>
	
using namespace std;

int main()

{

char c1,c2;
	
c1='a';
	
c2='b'; 
	
int i1,i2;
	
printf("%c,%d\n%c,%d",c1,c1,c2,c2);
	
return 0;
	
}

================================================================

######Exercise9(5月1號)

參考老師上課的內容

================================================================

#include <iostream>
	
using namespace std;



int main()

{

string s1("Welcome");
	
s1.append(" to CPP"); 

cout << s1 << endl; 

string s2("Welcome");

s2.append(" to C and Cpp", 3, 6); 

cout << s2 << endl;
	
string s3("Welcome");

s3.append(" to C and Cpp", 7); 

cout << s3 << endl; 

string s4("Welcome"); 

s4.append(14, 'F'); 

cout << s4 << endl; 
	
}
可以藉由append來取代一般字串的麻煩之處

s1：將s字串附加於this字串物件。[+append(s: string): string]

s2：將s字串的index位置開始n個字元，附加於this字串上。[+append(s: string, index: int, n: int): string]

s3：將s字串的前n個字元，附加於this字串上。[+append(s: string, n: int): string]

s4：將ch字元拷貝n次，然後附加於this字串。[+append(n: int, ch: char): string]

(參考課本C++程式設計導論內容!)

================================================================

######Exercise10(5月1號)

參考老師上課的內容

================================================================

#include <iostream>
	
using namespace std;


class ball

{

public:

  // The radius of this circle
  
  double radius;
  

  // Construct a default circle object
  
  ball()
  
  {
  
   radius = 1;
    
  }

  // Construct a circle object
  
  ball(double newRadius)
  
  {
  
   radius = newRadius;
    
  }

  // Return the area of this circle
  
  double getball()
  
  {
  
   return 4*radius * radius * 3.14159;
    
  }
  
};  // Must place a semicolon here

int main()

{

  ball ball1(1.0);
  
  ball ball2(25);
  
  ball ball3(125);
  

  cout << "The ball of the circle of radius "
  
   << ball1.radius << " is " << ball1.getball() << endl;
    
  cout << "The ball of the circle of radius "
  
   << ball2.radius << " is " << ball2.getball() << endl;
   
  cout << "The ball of the circle of radius "
  
   << ball3.radius << " is " << ball3.getball() << endl;

  // Modify circle radius
  
  ball2.radius = 100;
  
  cout << "The ball of the circle of radius "
  
   << ball2.radius << " is " << ball2.getball () << endl;

  return 0;
  
} 

================================================================

######Exercise11(5月1號)

參考老師上課的內容

================================================================

#include <iostream>
	
#include <string>

int main ()

{

  std::string str;
  
  std::string str2="Writing ";
  
  std::string str3="print 10 and then 5 more";
  

  // used in the same order as described above:
  
  str.append(str2);                       // "Writing "
  
  str.append(str3,6,3);                   // "10 "
  
  str.append("dots are cool",5);          // "dots "
  
  
  str.append("here: ");                   // "here: "
  
  str.append(10u,'.');                    // ".........."
  
  str.append(str3.begin()+8,str3.end());  // " and then 5 more"
  
  str.append<int>(5,0x2E);                // "....."

  std::cout << str << '\n';
  
  return 0;
  
}
================================================================

######Exercise12(5月1號)

作業參考

================================================================
#include <iostream>
	
#include <string>
	
using namespace std;

int main ()

{

string city;

cout << "Enter a city: ";

cin >> city; // Read to array city

cout << "You entered " << city << endl;

return 0;

}


![image](/PIC/string3.png "image")
================================================================
######Exercise13(5月1號)
老師指定作業
================================================================
#include <iostream>

#include <string>

using namespace std;

int main ()
{

string namenumber;

cout << "Enter you name and number: ";

cin >> namenumber;

cout << "You entered " <<  namenumber << endl;

return 0;

}

![image](/PIC/string4.png "image")

================================================================

######Exercise14:函數使用與呼叫(5月8號)

老師上課內容

================================================================
#include <iostream>
	
using namespace std;

void hello();

void old();

void number();


int main(void)

{

   hello();
    
   old();
    
   number();

   return 0;
}

void hello()

{

   cout << "Willy ";
    
}

void old()

{

   cout << " 現在 18 歲 ";
    
}

void number()

{

   cout << "學號:4060E011" << endl;
    
}

================================================================

######Exercise15:文件處理(5月8號)

老師上課內容

================================================================

#include <iostream>
	
#include <fstream>
	
using namespace std;

int main(void)

{

ofstream output("TEST.txt");

output << "Hello" << " " << "World" << " " << "20" << endl;

output << "Welcome" << " " << "CPP" << " " << "10" << endl;

output.close();

system("pause");

return 0;

}

================================================================

######Exercise16:字串處理(5月8號)

老師上課內容

================================================================

#include <iostream>
	
#include <string>
	
using namespace std;


int main(void)

{

  string str;
  
  string str2="Welcome ";
  
  string str3="print 10 and then 5 more";

  str.append(str2);     
  
  str.append(str3,9,4);   
  
  str.append("dots are cool",9);      
  
  str.append("here: ");    
  
  str.append(8u,'.');    
  
  str.append(str3.begin()+8,str3.end());  
  
  str.append<int>(5,0x2E);                

  cout << str << '\n';

  return 0;
  
}

================================================================

######Exercise17:製作類別bmi(5月15號)

老師上課內容

================================================================

如何用類別輕鬆製作BMI測量:

來源:參考老師上課內容

1. 建立一個定義BMI.h

#ifndef BMI_H

#define BMI_H

#include <string>

using namespace std;

class BMI

{

public:

  BMI(const string& newName, int newAge, double newWeight, double newHeight);
  
  BMI(const string& newName, double newWeight, double newHeight);
  
  double getBMI() const;
  
  string getStatus() const;
  
  string getName() const;
  
  int getAge() const;
  
  double getWeight() const;
  
  double getHeight() const;

private:

  string name;
  
  int age;
  
  double weight;
  
  double height;
  
};

#endif

2.製作一個實作BMI.cpp

#include <iostream>

#include "BMI.h"

using namespace std;

BMI::BMI(const string& newName, int newAge, 

  double newWeight, double newHeight)
  
{

  name = newName;
  
  age = newAge;
  
  weight = newWeight;
  
  height = newHeight;
  
}

BMI::BMI(const string& newName, double newWeight, double newHeight)

{

  name = newName;
  
  age = 20;
  
  weight = newWeight;
  
  height = newHeight;
  
}

double BMI::getBMI() const

{

  const double KILOGRAMS_PER_POUND = 0.45359237;
  
  const double METERS_PER_INCH = 0.0254;
  
  double bmi = weight * KILOGRAMS_PER_POUND /
  
   ((height * METERS_PER_INCH) * (height * METERS_PER_INCH));
    
  return bmi;
}

string BMI::getStatus() const

{

  double bmi = getBMI();
  
  if (bmi < 18.5)
  
    return "Underweight";
    
  else if (bmi < 25)
  
    return "Normal";
    
  else if (bmi < 30)
  
    return "Overweight";
    
  else
  
    return "Obese";
    
}

string BMI::getName() const

{

  return name;
  
}

int BMI::getAge() const

{

  return age;
  
}

double BMI::getWeight() const

{

  return weight;
  
}

double BMI::getHeight() const

{

  return height;
  
}

3.建立新專案 並可以開始使用類別 BMI1.cpp

#include <iostream>
  
#include "BMI.h"

using namespace std;

int main()

{

  BMI bmi1("John Doe", 18, 145, 70);
  
  cout << "The BMI for " << bmi1.getName() << " is "
  
   << bmi1.getBMI() << " " << bmi1.getStatus() << endl;

  BMI bmi2("Susan King", 215, 70);
  
  cout << "The BMI for " << bmi2.getName() << " is "
  
   << bmi2.getBMI() << " " + bmi2.getStatus() << endl;

  return 0;
  
}


##  End:

![END](/PIC/專案.png "END")

================================================================

######Exercise18:整數堆疊(5/22)

參考老師上課內容

================================================================

整數堆疊

1]定義 ==> StackOfIntegers.h

#ifndef STACK_H

#define STACK_H



class StackOfIntegers

{

public:

  StackOfIntegers();
  
  bool isEmpty() const;
  
  int peek() const;
  
  void push(int value);
  
  int pop();
  
  int getSize() const;
  

private:

  int elements[100];
  
  int size;
  
};

#endif

[2]實作==> StackOfIntegers.cpp

#include "StackOfIntegers.h"

StackOfIntegers::StackOfIntegers()

{

  size = 0;
  
}

bool StackOfIntegers::isEmpty() const

{

  return (size == 0);
  
}

int StackOfIntegers::peek() const

{

  return elements[size - 1];
  
}


void StackOfIntegers::push(int value)

{

  elements[size++] = value;
  
}

int StackOfIntegers::pop()

{

  return elements[--size];
}

int StackOfIntegers::getSize() const

{

  return size;
  
}

[3]使用==>TestStackOfIntegers.cpp

#include <iostream>

#include "StackOfIntegers.h"

using namespace std;


int main()

{
  StackOfIntegers stack;

  for (int i = 0; i < 10; i++)
  
   stack.push(i);

  while (!stack.isEmpty())
  
   cout << stack.pop() << " ";

  return 0;
  
}

##  End1:

![END1](/PIC/sTAck1.png "END1")

================================================================

######Exercise19:整數+字串堆疊(5/22)

參考老師上課內容

================================================================

字串+整數堆疊

[1]定義+實作 ==> GenericStack.h

#ifndef STACK_H

#define STACK_H

template<typename T>
  
class Stack
  
{
  
public:
  
  Stack();
  
  bool empty() const;
  
  T peek() const;
  
  void push(T value);
  
  T pop();
  
  int getSize() const;
  

private:

  T elements[100];
  
  int size;
  
};

template<typename T>
  
Stack<T>::Stack()
  
{
  
  size = 0;
  
}

template<typename T>
  
bool Stack<T>::empty() const
  
{
  
  return (size == 0);
  
}

template<typename T>
  
T Stack<T>::peek() const
  
{
  
  return elements[size - 1];
  
}

template<typename T>
  
void Stack<T>::push(T value)
  
{

  elements[size++] = value;
  
}

template<typename T>
  
T Stack<T>::pop()
  
{
  
  return elements[--size];
  
}

template<typename T>
  
int Stack<T>::getSize() const
  
{
  
  return size;
  
}

#endif

[2]使用==>TestGenericStack.cpp

#include <iostream>
  
#include <string>
  
#include "GenericStack.h"
  
using namespace std;
  

int main()

{

  // Create a stack of int values
  
  Stack<int> intStack;
  
  for (int i = 0; i < 10; i++)
                         
   intStack.push(i);
                         

  while (!intStack.empty())
  
  cout << intStack.pop() << " ";
    
  cout << endl;
  

  // Create a stack of strings
  
  Stack<string> stringStack;
  
  stringStack.push("Chicago");
  
  stringStack.push("Denver");
  
  stringStack.push("London");
  

  while (!stringStack.empty())
  
   cout << stringStack.pop() << " ";
    
  cout << endl;
  

  return 0;
  
}

##  End2:

![END2](/PIC/sTAck2.png "END2")


================================================================

######Exercise20:檔案的輸入(6/5)

老師上課內容

================================================================

#include <iostream>

#include <fstream>

using namespace std;

int main()

{

  ofstream output;
  

  // Create a file
  
  output.open("d:///scores.txt");

  // Write two lines
  
  output << "John" << " " << "T" << " " << "Smith" 
  
   << " " << 90 << endl;
    
  output << "Eric" << " " << "K" << " " << "Jones" 
  
   << " " << 85 << endl;
    
  output << "中文" << " " << "也" << " " << "可以" 
  
   << " " << 100 << endl;
  
  output << "NTOU" << " " << "絕對" << " " << "通過" 
  
   << " " << 1000 << endl; 
    
  output.close();

  cout << "Done" << endl;

  return 0;
  
}

##  PUT:

![PUT](/PIC/PUT1.png "PUT")

================================================================

######Exercise21:檔案的輸出(6/5)

老師上課內容

================================================================

#include <iostream>
  
#include <fstream>
  
#include <string>
  
using namespace std;
  

int main()

{

  ifstream input("d:/// scores.txt");

  // Read data
  
  string firstName;
  
  char mi;
  
  string lastName;
  
  int score;
  
  input >> firstName >> mi >> lastName >> score;
  
  cout << firstName << " " << mi << " " << lastName << " "
  
   << score << endl;

  input >> firstName >> mi >> lastName >> score;
  
  cout << firstName << " " << mi << " " << lastName << " "
  
   << score << endl;

 input >> firstName >> mi >> lastName >> score;
 
  cout << firstName << " " << mi << " " << lastName << " "
  
   << score << endl;
    
   input >> firstName >> mi >> lastName >> score;
     
  cout << firstName << " " << mi << " " << lastName << " "
  
   << score << endl;
    
  input.close();

  cout << "Done" << endl;

  return 0;
  
}

##  out:

![out](/PIC/out1.png "out")

================================================================

######Exercise22:如何把檔案存取到C槽(6/5)

老師上課內容

================================================================

首先，先以系統管理員的身分開啟命令提示字元:

## OK:

![OK](/PIC/正確1.png "OK")

再來輸入CPP程式碼的存放位置，以系統管理員的身分開啟，接著執行便可在C槽新增檔案:

##  OK2:

![OK2](/PIC/正確2.png "OK2")

接著也可以讀取到C槽的檔案了:

##  OK3:

![OK3](/PIC/正確3.png "OK3")

================================================================

######Exercise23:偵測檔案是否存在(6/5)

老師上課內容

================================================================

#include <iostream>
	
#include <fstream>
	
using namespace std;
	

int main()

{

  // Open a file
  
  ifstream input("d:///score.txt");
  
  // 檢查檔案是否存在==>使用fail()
  
  if (input.fail())
  
  {
  
   cout << "File does not exist" << endl;
    
   cout << "Exit program" << endl;
    
   return 0;
    
  }

  double sum = 0;
  
  double number;
  
  
  //參看課本不同做法與錯誤分析
  
  while (input >> number) // Read data to the end of file
  
  {
  
   cout << number << " "; // Display data
   
   sum += number;
    
  }
  
  //
  
  input.close();

  cout << "\nTotal is " << sum << endl;

  return 0;
  
}

輸入正確時:

##  fail:

![fail](/PIC/fail.png "fail")

輸入錯誤時:

##  failno:

![failno](/PIC/failfail.png "failno")

================================================================

######Exercise24:查詢檔案是否存在的程式碼(6/5)

老師上課內容

================================================================



#include <iostream>
	
#include <fstream>
	
#include <string>
	
using namespace std;
	

int main()

{

  string filename;
  
  cout << "Enter a file name: ";
  
  cin >> filename;
  

  ifstream input(filename.c_str());
  
  if (input.fail())
  
   cout << filename << " does not exist" << endl;
    
  else
  
   cout << filename << " exists" << endl;

  return 0;
  
}

##  fail2:

![fail2](/PIC/fail2.png "fail2")

================================================================

######Exercise25:

================================================================
