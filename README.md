# Brainwave_Matrix_Intern-    TASK 1
Fully Functional ATM Interface



# include <iostream>
# include <stdlib.h>
# include<string>
using namespace std;
class atm {

    private:
    string name;
    long long accnumber;
    char type[10];
    long long amount=0;
    long long total=0;


    public:
    void setvalue(){
        cout<<"enter name\n";
        cin.ignore();

        getline(cin,name);

        cout<<"enter account number\n";
        cin>> accnumber;

        cout<< "enter account type\n";
        cin>> type;

        cout<<"enter the balance\n";
        cin>>total;
    }

    void showdata(){
        cout<<"name"<<name<<endl;
        cout<<"account number"<<accnumber<<endl;
        cout<<"account type"<<type<<endl;
        cout<<"balance"<<total<<endl;
        
    }
    void deposit(){
        cout<<"enter the amount to be deposited\n";
        cin>>amount;
    }
    void showbalance(){
        total=total+amount;
        cout<<"\n total balance is--> "<<total;
    }

    void withdrawl(){
        int a,avlbal;
        cout<<"enter the amout you want to withdrawal\n";
        cin>>a;
        avlbal=total-a;
        cout<<"availaible balance"<<avlbal;
    }


};
int main(){
    atm c;
    int choice;

    while (1){
        cout<<"\n -----------------------------------------------WELCOME------------------------------------------\n";
        cout<<"enter your choice\n";
        cout << "\t1. Enter name, Account "
             << "number, Account type\n";
        cout << "\t2. Balance Enquiry\n";
        cout << "\t3. Deposit Money\n";
        cout << "\t4. Show Total balance\n";
        cout << "\t5. Withdraw Money\n";
        cout << "\t6. Cancel\n";
        cin >> choice;


         switch (choice) {
        case 1:
            c.setvalue();
            break;
        case 2:
            c.showdata();
            break;
        case 3:
            c.deposit();
            break;
        case 4:
            c.showbalance();
            break;
        case 5:
            c.withdrawl();
            break;
        case 6:
            exit(1);
            break;
        default:
            cout << "\nInvalid choice\n";
        }
    }
}



