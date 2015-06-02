#include "stdafx.h" //для visual studio. чтобы он знал, какие файлы скомпилировал, чтобы не компил. их вновь.
#include <iostream> //подключение библиотеки ввода - вывода
#include <cstdlib> //подключение библиотеки выделения памяти
#include <ctime> //библиотека времени. дабы случайные числа гененировались при каждом запуске программы в разное время разные
using namespace std; //открытие пространства стандартных имён библиотеки
int main()
{
int n, i, min, max; 
float sr; 
float sred; 
srand((int)time(NULL)); 
cout << "enter size of the array:"; 
cin>> n; 
int *array = new int [n]; 
for (i=0; i<n; i++) 
	{array[i]=(rand()%199-99); 
	cout << array[i] << " ";}
	system("pause"); 
sred = 0;
for (i=0; i<n; i++) 
	{sred+=array[i];} 
	sr=sred/n; 
	cout <<"the arithmetic mean of the array is equal to: " << sr << " "; 
	system("pause"); 
	max = array[0];
	min = array[0];
for (i=0; i<n; i++)
	{if (array[i] < min) min = array[i];
     if (array[i] > max) max = array[i];}
	cout << "the minimum value of the array element is equal to: " << min << " "; 
	cout << "the maximum value of the array element is equal to: " << max << " "; 
	system("pause");
	return 0;
}
