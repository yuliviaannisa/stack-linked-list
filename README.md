#include <iostream>
#define MAX_STACK_SIZE 10
using namespace std;

struct Element{
    int data;
    Element *next;
};

class MyStack {
    private:
	Element *head=NULL;

    public:
    bool isEmpty(){
        if(head==NULL){
        	return 1;
          }
        	else return 0;
		}

    void push(int databaru){
			Element *baru=new Element;
	    	baru->head=databaru;
	        baru->next=data;
	        head=baru;
	        cout<<"Data Masuk\n"<<endl;
    }
    void pop(){
    	if(isEmpty()==false){
    		Element *baru=new Element;
    		baru=head;
			head=head->next;
			delete baru;
			cout<<"Data pop\n"<<endl;
        } else {
            cout<<"tidak ada stack"<<endl;
        }
    }
    void printStackList(){
    	Element *bantu;
    	bantu=head;

        if (isEmpty()==false){
            while(head!=NULL){
            	cout<<bantu->data<<endl;
            	bantu=bantu->next;
			}
        } else {
            cout<<"tidak ada stack"<<endl;
        }
    }
    int getTop(){
    	Element *top=head;
        return top->data;
    }
};

int main()
{
    MyStack y;
    int x;
	int databaru;
	do{
		cout<<"linked List on Stack"<<endl;
		cout<<"-----------"<<endl<<endl;
		cout<<"1.Push"<<endl;
		cout<<"2.Pop"<<endl;
		cout<<"3.Top Stack"<<endl;
		cout<<"4.Tampilkan Stack"<<endl;
		cout<<"5.Exit"<<endl;
		cout<<"pilihan anda : ";
		cin>>x;
		switch(x){
			case 1:cout<<endl;
			cout<<"data: ";
			cin>>databaru;
			cout<<endl;
			y.push(databaru);break;

			case 2:
			cout<<endl;
			y.pop();
			break;

			case 3:
			cout<<endl;
			if(y.isEmpty()==false){
			cout<<y.getTop()<<endl;
			}else{
				cout<<"tidak ada stack";
				}
			cout<<endl;break;

			case 4:
			cout<<endl;
			y.printStackList();
			break;

			default:cout<<"\tselesai";

		}
	}
while (x!=5);
}
