//# protected-public-private-access
//oop c++ Inheritance public ,protected and private access
//public , private , Protected data members access  
#include<iostream>
using namespace std;
class NumberP{
	public:
		int x;
	private:
		int y;
	
	protected:
	    int z;
};
class Child1:public NumberP{
	public:
	Child1(){
	cout<<"Enter the value of X : "<<endl;
	cin>>x;
	cout<<"public x= "<<x<<endl;
	}
	
};
class Child2:private NumberP{
	public:
	Child2(){
	
	
	
	cout<<"privat y can't access "<<endl;
	}
	
};
class Child3:protected NumberP{
	public:
	Child3(){
	
	cout<<"Enter the value of Z : "<<endl;
	cin>>z;
	cout<<"protected z= "<<z<<endl;
	}
	
};

int main(){
	Child1 c1;
	Child2 c2;
	Child3 c3;
	
	return 0;
}
