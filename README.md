#include<algorithm>
#include<math.h>
#include<iostream>
using namespace std;
string root(int root);
string exponent(int exponent);
int main()
{
	long rootNum, exponentNum;
	cout << " Kindly enter the value you want the Root Number of : ";
	cin >> rootNum;
	while(cin.fail())
	{
		cin.clear();
		cin.ignore(1000, '\n');
		cout << "Invalid Value \nTry Again: ";
		cin >> rootNum;
	}
	cout << root(rootNum) << endl << endl;
	cout << "Kindly enter the value you want the Exponent for : ";
	cin >> exponentNum;
	while (cin.fail())
	{
		cin.clear();
		cin.ignore(1000, '\n');
		cout << "Invalid Value \nTry Again: ";
		cin >> exponentNum;
	}
	cout << exponent(exponentNum) << endl;
	return 0;
}
string root(int root)
{
	string Statement = "It is All Great! The Code is Operating.";
	for (float i = 2; i <= 10; i++)
	{
		float Answer = pow(root, 1/i);
		cout << i << " root of " << root << " is: " << Answer << endl;
	}
	return Statement;
}
string exponent(int exponent)
{
	string Statement = "It is All Great! The Code is Operating";
	for (int i = 1; i <= 10; i++)
	{
		long Answer = pow(exponent, i);
		cout << i << " exponent of " << exponent << " is: " << Answer << endl;
	}
	return Statement;
}
