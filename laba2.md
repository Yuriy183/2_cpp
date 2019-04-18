/* Лабораторная работа №2 - Обработка динамических структур в С/C++ 
3) "Студент":
фамилия, имя, отчество, пол, национальность, рост, вес, дата рождения(год, месяц, число), номер телефона,
домашний адрес(почтовый индекс, страна, область, район, город, улица, дом, квартира), ВУЗ, курс, группа,
средний бал, специальность. */

#include "pch.h"
#include <iostream>
#include <conio.h>
#include <string>

using namespace std;

struct DATE // рождение
{
	unsigned short day;
	unsigned short mounth;
	unsigned short year;
};

struct HOMEADRESS // домашний адресс и всё связаное с ним
{
	unsigned short postcode; // почтовый индекс
	unsigned short country; // страна
	string region; // область
	string district; // район
	string city; // город
	string street; // улица
	unsigned short house; // дом
	unsigned short apartment; // квартира

};

struct laba2 { 

	string surname; // фамилия
	string name;  // имя
	string patronymic; // отчество
	string sex; // пол
	string nationality; // национальность
	unsigned short height; // рост
	unsigned short weight; // вес
	DATE date; // рождение
	unsigned long number_phone; // номер телефона
	HOMEADRESS home_adress; // дом.адресс
	string university; // ВУЗ
	unsigned short course; // курс
	unsigned short group; // группа
	unsigned short average_ball; // средний бал
	 string specialty; // специальность
};

int main() {
	setlocale(LC_ALL, "RUS");
	const int n = 2; // заданиe количества стуктур в массиве 
	laba2 arr[n]; // массив структуры

	for (int i = 0; i < n; i++) {
		cout << "Введите фамилию: ";
		getline(cin, arr[i].surname);
		cout << "Введите имя: ";
		getline(cin, arr[i].name);
		cout << "Введите отчество: ";
		getline(cin, arr[i].patronymic);
		cout << "Введите пол: ";
		getline(cin, arr[i].sex);
		cout << "Введите национальность: ";
		getline(cin, arr[i].nationality);
		cout << "Введите рост: ";
		cin >> arr[i].height;
		cout << "Введите вес: ";
		cin >> arr[i].weight;
		cout << "Введите день рождения: " << endl;
		cin >> arr[i].date.day;
		cout << "Введите месяц рождения: " << endl;
		cin >> arr[i].date.mounth;
		cout << "Введите год рождения: " << endl;
		cin >> arr[i].date.year;
		cout << "Введите номер телефона" << endl;
		cin >> arr[i].number_phone;
		
	}
}
