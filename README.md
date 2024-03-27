[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Fmb6W2KK)
Design a C++ program for an employee payroll system. Create classes for Employee and Payroll. Users can add employees, enter hours worked, calculate salaries, and generate payroll reports.

#include <iostream>
#include <string>
using namespace std;

class employee {
public:
    string name;
    int id;
    double hour_worked;
    double hourly_rate;
    double salary;
    double gross_deduction;

    void set_data() {
        cout << "Enter employee name: ";
        cin >> name;
        cout << "Enter employee ID: ";
        cin >> id;
        cout << "Enter employee hour worked: ";
        cin >> hour_worked;
        cout << "Enter employee hourly rate: ";
        cin >> hourly_rate;
        cout << "Enter gross deduction: ";
        cin >> gross_deduction;
    }

    double calculate_income() {
        salary = hourly_rate * hour_worked;
        return salary;
    }

    double get_salary() const {
        return salary;
    }

    double get_gross_deduction() const {
        return gross_deduction;
    }
};

class payroll {
public:
    double payroll_;

    void pay_roll(employee &em) {
        payroll_ = em.get_salary() - em.get_gross_deduction();
        cout << "Payroll: " << payroll_ << endl;
    }
};

int main() {
    employee e[200];
    payroll p[200];
    int employee_list;

    cout << "Enter number of employees: ";
    cin >> employee_list;

    for (int i = 0; i < employee_list; i++) {
        cout << "\nEnter details for employee " << i+1 << ":" << endl;
        e[i].set_data();
    }

    for (int i = 0; i < employee_list; i++) {
        cout << "\nPayroll details for employee " << i+1 << ":" << endl;
        cout << "--------------------------" << endl;
        e[i].calculate_income();
        p[i].pay_roll(e[i]);
    }

    return 0;
}
