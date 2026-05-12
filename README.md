#include<iostream>
using namespace std;
class Payment{
    public:
    void makePayment(int amount){
        cout<<"Payment of Rs."<<amount<< " done using Cash"<<endl;
    }
    void makePayment(string cardNumber, int amount){
        cout<<"Payment of Rs."<<amount<< " done using Card:"<<cardNumber<<endl;
    }
    void makePayment(string upiID,double amount){
        cout<<"Payment of Rs."<<amount<< " done using UPI:"<<upiID<<endl;
    }
};
int main(){
    Payment p;
    p.makePayment(500);//cash
    p.makePayment("1234-5678-9012",1000);//card
    p.makePayment("user@upi",250.75);//upiid
    return 0;
}
