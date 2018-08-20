���������������� ���������� ������ String (�.�. �������� string1.h ��
string2.h), �������� ������������� ���� ��������.
	�. ����������� �������� + ��� ����������� ���� ����� � ����.
������ � ������������ ��������� ������ 
	�. �������� �������-���� stringlow(), ������� ����������� ��� ���������
������� � ������ � ������ �������. (�� �������� � ��������� cctype ����������
�������.)
	�. �������� �������-���� stringup(), ������� ����������� ��� ���������
������� � ������ � ������� �������. '
	�. �������� �������-����, ������� ��������� �������� ���� char � ����������
���������� ���, ������� ������ ���������� � ������.
��������� ������ ����������� ������ � ��������� ���������:

#include <iostream>
using namespace std;
#include "string2.h"
int main()
{
	String si(" and I am a C++ student.");
	String s2 = "Please enter your name: ";
	String s3;
	cout << s2;
	cin >> s3;
	s2 = "My name is " + s3;
	cout << s2 << ".\n";
	s2 = s2.operator+(si);
	s2.stringup();
	cout << "The string\n" << s2 << "\ncontains " << s2.has('A')
		<< " 'A' characters in it.\n";
	si = "red";
	String rgb[3] = { String(si), String("green"), String("blue") };
	cout << "Enter the name of a primary color for mixing light: ";
	String ans;
	bool success = false;
	while (cin >> ans) {
		ans.stringlow();
		for (int i = 0; i < 3; i++)
		{
			if (ans == rgb[i])
			{
				cout << "That's right!\n";
				success = true;
				break;
			}
		}
		if (success)
			break;
		else
			cout << "Try again! \n";
	}
	cout << "Bye\n";
	return 0;
}

dankor1498 
�������������� - MVS 2017.
dankor1498@gmail.com