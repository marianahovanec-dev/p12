# p12
Завдання 1 

#include <fstream>
#include <string>
#include <iostream>
using namespace std;

int main() {
    ofstream fout("students.txt"); 
    string name = "Іваненко Іван";
    double grade = 95;

    fout <<name << "," << grade << endl; // запис
    fout.close();

    ifstream fin("students.txt");
    string line;
    while (getline(fin, line)) { // читання рядка
        cout << line << endl;
    }
    fin.close();
}
[UploaІваненко Іван,95
ding students.txt…]()

Завдання 2

#include <fstream>
#include <string>
#include <iostream>
using namespace std;

int main() {
    ofstream fout("students.txt"); 
    string name = "Іваненко Іван";
    double grade = 95;

    fout <<name << "," << grade << endl; // запис
    fout.close();

    ifstream fin("students.txt");
    string line;
    while (getline(fin, line)) { // читання рядка
        cout << line << endl;
    }
    fin.close();
    
    ofstream fout2("students.txt", ios::app); // режим дописування
    fout << "Петренко Олена,87" << endl;
    fout2.close();
}
Іваненко Іван,95

Завдання 3 

#include <fstream>
#include <iostream>
using namespace std;

int main() {
    ifstream fin("numbers.txt");
    int n, sum = 0;

    while (fin >> n) { // зчитування числа
        sum += n;
    }

    cout << "Сума чисел: " << sum << endl;
    fin.close();
}

1 2 3 4 5
