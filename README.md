# A-code-for-login
A code to login to the system. You can use this code for larger codes and perform login operations with this piece of code.
#include<iostream>
#include<conio.h>
#include<string.h>
using namespace std;
class person
{
	private :
	char first_name[15];
	char last_name[20];
	char password[16];
	int age;
	string login_month;
	int login_day;
	char phone_number[14];
	public :
	void setall (char *a,char *b,int c,string d,int e,char *f,char *g){
	strcpy(first_name,a);
	strcpy(last_name,b);
	age=c;
	login_month=d;
	login_day=e;
	strcpy(phone_number,f);
	strcpy(password,g);
	}
};
int main()
{
	char phone_number_code[14];
	char first_name_code[15];
	char last_name_code[20];
	char password_code[16];
	string login_month_code;
	int login_day_code;
	int been_int[8]={0,0,0,0,0,0,0,0};
	int age_code;
	cout<<"your first name : ";
	cin.getline(first_name_code,15);
	int eae=strlen(first_name_code);
	if (eae<=2){
		cout<<"enter your real first name !"<<endl;
		cout<<"enter your first name again : ";
		cin.getline(first_name_code,15);
		int yy=strlen(first_name_code);
		if (yy<=2){
			cout<<"you has been";
			been_int[0]++;
		 }
		}
	if (been_int[0]==0){
	cout<<"your last name : ";
	cin.getline(last_name_code,20);
	int ee=strlen(last_name_code);
	if (ee<=2){
		cout<<"enter your real last name !"<<endl;
		cout<<"enter your last name again : ";
		cin.getline(last_name_code,20);
		int yyu=strlen(last_name_code);
		if (yyu<=2){
			cout<<"you has been";
			been_int[1]++;
		}
	}
	if (been_int[1]==0){
	int e=strcmp(first_name_code,last_name_code);
	if (e==0){
		cout<<"enter your real first and last name ! ";
		cout<<endl;
		cout<<"enter your first name again : ";
	cin.getline(first_name_code,15);
	cout<<"enter your last name again : ";
	cin.getline(last_name_code,20);
	int ooo=strcmp(first_name_code,last_name_code);
	if (ooo==0){
		cout<<"you has been";
		been_int[6]++;
	}
	}
	if (been_int[6]==0){
	cout<<"build your password : ";
	cin.getline(password_code,16);
	int pl=strlen(password_code);
	if (pl<8){
		cout<<"password should not be smaller than 8 words";
		cout<<endl;
		cout<<"build your new password : ";
		cin.getline(password_code,16);
		int pla=strlen(password_code);
	if (pla<8){
		cout<<"password should not be smaller than 8 words";
		cout<<endl;
		cout<<"build your new password againe : ";
		cin.getline(password_code,16);
		int plb=strlen(password_code);
		if (plb<8){
			cout<<"you has been";
			been_int[7]++;
		}
		}
	}
	if (been_int[7]==0){
	cout<<"your age : ";
	cin>>age_code;
	if(age_code>120	or	age_code<=3){
		cout<<"enter your real age ! "<<endl;
		cout<<"enter your age again : ";
		cin>>age_code;
		if(age_code>120	or	age_code<=3){
			cout<<"you has been";
			been_int[2]++;
		}
	}
	if (been_int[2]==0){
	cout<<"phone number (+ _ _ - - - - - - - - - -) : ";
	cin.getline(phone_number_code,14);
	cin.getline(phone_number_code,14);
	int pp=strlen(phone_number_code);
	for (int i=1;i<=13;i++){
	if (phone_number_code[0]!='+'	or	pp<13	or	phone_number_code[i]>'A'	&&	phone_number_code[i]<'z'){
		cout<<"enter your real phone number ! "<<endl;
		cout<<"enter your phone number again : ";
		cin.getline(phone_number_code,14);
		int ppo=strlen(phone_number_code);
		if (phone_number_code[0]!='+'	or	pp<13	or	phone_number_code[i]>'A'	&&	phone_number_code[i]<'z'){
			cout<<"you has been";
			been_int[3]++;
			break;
		}
	}
	}
	if (been_int[3]==0){
	cout<<"login day : ";
	cin>>login_day_code;
	if (login_day_code<=0	or	login_day_code>31){
		cout<<"enter your real login dey ! "<<endl;
		cout<<"enter your login day again : ";
		cin>>login_day_code;
		if (login_day_code<=0	or	login_day_code>31){
			cout<<endl<<"you has been";
			been_int[4]++;
		}
	}
	if (been_int[4]==0){
		cout<<"login month (with small words) : ";
		cin>>login_month_code;
		if (login_month_code=="january"	or	login_month_code=="february"	or	login_month_code=="march"	or	login_month_code=="april"	or	login_month_code=="may"	or	login_month_code=="june"	or	login_month_code=="july"	or	login_month_code=="august"	or	login_month_code=="september"	or	login_month_code=="october"	or	login_month_code=="november"	or	login_month_code=="december"){
			cout<<"login was successful";
		}
		else {
			cout<<"enter real login month ! "<<endl;
			cout<<"enter your login month again : ";
			cin>>login_month_code;
			if (login_month_code=="january"	or	login_month_code=="february"	or	login_month_code=="march"	or	login_month_code=="april"	or	login_month_code=="may"	or	login_month_code=="june"	or	login_month_code=="july"	or	login_month_code=="august"	or	login_month_code=="september"	or	login_month_code=="october"	or	login_month_code=="november"	or	login_month_code=="december"){
			cout<<endl<<endl<<endl<<"login was successful"<<endl;
		}
		else {
			cout<<"you has been";
			been_int[5]++;
		}
		}
		if (been_int[5]==0){
	person user1;
	user1.setall(first_name_code,last_name_code,age_code,login_month_code,login_day_code,phone_number_code,password_code);
	getch();
	return 0;
	}
	}
	}
	}
	}
	}
	}
	}
	for (int i=0;i<8;i++){
		if(been_int[i]==1){
			cout<<endl<<endl<<endl<<endl<<"do you want more details? (yes or no)"<<endl;
			string detail;
			cin>>detail;
			if (detail=="no"	or	detail=="No"	or	detail=="NO"){
				cout<<"ok";
			}
			else if (detail=="yes"	or	detail=="sure"	or	detail=="Yes"	or	detail=="YES"){
				if (been_int[0]>0){
					cout<<endl<<"You entered the first name incorrectly several times"<<endl;
				}
				else if (been_int[1]>0){
					cout<<endl<<"You entered the last name incorrectly several times"<<endl;
				}
				else if (been_int[2]>0){
					cout<<endl<<"You entered your age incorrectly several times"<<endl;
				}
				else if (been_int[3]>0){
					cout<<endl<<"You entered the wrong phone number several times"<<endl;
				}
				else if (been_int[4]>0){
					cout<<endl<<"You entered your login day incorrectly several times"<<endl;
				}
				else if (been_int[5]>0){
					cout<<endl<<"You entered your login month incorrectly several times"<<endl;
				}
				else if (been_int[6]>0){
					cout<<endl<<"You entered your first name and last name incorrectly several times"<<endl;
				}
				else if (been_int[7]>0){
					cout<<endl<<"You entered your password incorrectly several times"<<endl;
				}
		}
			else {
			cout<<"You have to choose between yes and no !"<<endl;
			}
		}
	}
};
