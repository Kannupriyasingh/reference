# reference
#include <iostream>

using namespace std;

int main()
{
    int a =10,&b=a; //b is the [reference]of a

    //a and b have the same memory
    cout <<"a=" <<a << "," <<"b=" << b << endl;
    cout<<"&a="<<&a <<"," << "&b="<< &b <<endl;

    ++a; //changing the appears as in b
    cout << "a="<<a <<"," << "b="<< b<< endl;

    ++b;//changing the appears as in a
    cout <<"a=" << a<<"," <<"b="<< b<< endl;

    return 0;
}
 void funki( //function prototype        //void funki(int &b,int c)
 int &b, //reference parameter
 int c); //value parameter
  int main()
  {
      int a=20;
      cout <<"a="<<a <<","<<"&a=" <<&a<<endl;
      funki(a,a);//function call
      return 0;
  }
void funki (int &b,int c)
{
    cout <<"b="<<b <<"," <<"&b="<<&b<< endl;
    cout <<"c="<<c <<"," <<"&c="<<&c<< endl;
}

void swap(int&,int&);  //call by reference
int main()
{
    int a,b;
    a=10,b=60;
    cout<<"a="<<a<<","<<"b="<<b<<endl;
    swap(a,b);
    cout<<"a="<<a<<","<<"b="<<b<<endl;
    int c=98,d=54;
     cout<<"c="<<c<<","<<"d="<<d<<endl;
     swap(c,d);
    cout<<"c="<<c<<","<<"d="<<d<<endl;
    return 0;

}
void swap (int &x,int &y)
{
    int t;
    t=x;                       //  output a=10,b=60
    x=y;                         //a=60,b=10
    y=t;
}
