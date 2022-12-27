#include<iostream>
#include<fstream>
#include<string.h>
#include <sstream>
#include<graphics.h>
#include <vector>

//**********************************************************************************************************************************************************************************

using namespace std;
void loginadmin();
void login();
void registration();
void registrationadmin();
void bookFlight();
void editUserInfo();
void deleteAccount();

int main()
{
int choice;
	cout << endl;
	cout << endl;
	cout <<"                                                                                                                                                                                                        " <<endl;
	cout <<"   888       888          888                                              888                 888888b.          d8888 888     888              d8888 d8b         888 d8b                           " << endl;
	cout <<"   888   o   888          888                                              888                 888  '88b        d88888 888     888             d88888 Y8P         888 Y8P                           " << endl;
	cout <<"   888  d8b  888          888                                              888                 888  .88P       d88P888 888     888            d88P888             888                               " << endl;
	cout <<"   888 d888b 888  .d88b.  888  .d8888b  .d88b.  88888b.d88b.   .d88b.      888888  .d88b.      8888888K.      d88P 888 Y88b   d88P           d88P 888 888 888d888 888 888 88888b.   .d88b.  .d8888b " << endl;
	cout <<"   888d88888b888 d8P  Y8b 888 d88P'    d88''88b 888 '888 '88b d8P  Y8b     888    d88''88b     888  'Y88b    d88P  888  Y88b d88P      d88P  888 888 888P'   888 888 888 '88b d8P  Y8b 88K     " << endl;
	cout <<"   88888P Y88888 88888888 888 888      888  888 888  888  888 88888888     888    888  888     888    888   d88P   888   Y88o88P     d88P   888 888 888     888 888 888  888 88888888 'Y8888b." << endl;
	cout <<"   8888P   Y8888 Y8b.     888 Y88b.    Y88..88P 888  888  888 Y8b.         Y88b. Y88...88P     888   d88P  d8888888888    Y888P      d8888888888 888 888     888 888 888  888 Y8b.          X88" << endl;
	cout <<"   888P     Y888  'Y8888  888  'Y8888P  'Y88P'  888  888  888  'Y8888      'Y888  'Y88P'       8888888P'  d88P     888     Y8P       d88P     888 888 888     888 888 888  888  'Y88888  88888P'" << endl;
	cout <<"                                                                                                                                                                                                        " <<endl;                                                                                                                                                                                                         
	cout<<"\t\t\t\t+++++++++Welcome to BAV Airlines+++++++++\n\n\n"<<endl;
	cout<<"To Futher Proceed, Please enter a value.\n"<<endl;
	cout<<"****Default Username && Password is root-root **** Using Default Credentials will restrict you to just view the list a Passenger...\n\n\n"<<endl;
	cout<<"\t (a) Press 0 to Exit                           "<<endl;
	cout<<"\t (b) Press 1 to Login as admin.                "<<endl;
	cout<<"\t (c) Press 2 to Register as admin.             "<<endl;
	cout<<"\t (d) Press 3 to Login as Passenger.            "<<endl;
	cout<<"\t (e) Press 4 to Register as Passenger.         "<<endl;
	cout<<"\t (f) Press 5 to Display the User Manual.       "<<endl;
	cout<<"\t Enter the desired option: ";
	cin>>choice;
	cout<<endl;
	
	switch(choice)
	{
		case 0:
			cout<<"Thanks for using this program.\nThis program is created by 2 newbie\n";
			Sleep(3000);
			exit(1);
			break;
		case 1:
			loginadmin();
			break;
		case 2:
			registrationadmin();
			break;
		case 3:
			login();
			break;
		default:
			system("cls");
			cout<<"\t\t\t Please select from the options given above \n"<<endl;
			main ();
		case 4:
			registration();
			break;
	}
}
//**************************************************************************************************************************************************
void loginadmin()
{
		int count;
		string userIdadmin, password, idadmin, pass;
//system("cls");
	cout <<"                                                                                                         " <<endl;
	cout <<"              .d8b.  d8888b. .88b  d88. d888888b d8b   db      db       .d88b.   d888b  d888888b d8b   db" <<endl;
	cout <<"              d8' `8b 88  `8D 88'YbdP`88   `88'   888o  88      88      .8P  Y8. 88' Y8b   `88'   888o  88" <<endl;
	cout <<"              88ooo88 88   88 88  88  88    88    88V8o 88      88      88    88 88         88    88V8o 88" <<endl;
	cout <<"              88~~~88 88   88 88  88  88    88    88 V8o88      88      88    88 88  ooo    88    88 V8o88" <<endl;
	cout <<"              88   88 88  .8D 88  88  88   .88.   88  V888      88booo. `8b  d8' 88. ~8~   .88.   88  V888" <<endl;
	cout <<"              YP   YP Y8888D' YP  YP  YP Y888888P VP   V8P      Y88888P  `Y88P'   Y888P  Y888888P VP   V8P" <<endl;
	cout <<"                                                                                                          " <<endl;
	cout <<"                                                                                                          " <<endl; 
	cout<<"Enter the  Username to login to the Management System: "<<endl;
	cin>>userIdadmin;
	cout<<"Enter the Password to login to the Management System: ";
	cin>>password;
		
	ifstream input("admin.txt");
		
	while(input>>idadmin>>pass)
	{
	if(idadmin==userIdadmin && pass==password)
		{
			count=1;
			system("cls");
		}
			}
	input.close();
		
	if(count==1)
	{
		int choice;
		cout<<userIdadmin<<"\n Your LOGIN is successfully as (admin)... For further Proceedings, enter a value from below...\n"<<endl;
	cout <<"                                                                                                                                                                    " <<endl;
	cout << "           d88888b db      db    db d888888b d8b   db  d888b       db   d8b   db d888888b d888888b db   db      d888888b d8888b. db    db .d8888. d888888b " <<endl;
	cout << "           88'     88      `8b  d8'   `88'   888o  88 88' Y8b      88   I8I   88   `88'   `~~88~~' 88   88      `~~88~~' 88  `8D 88    88 88'  YP `~~88~~'" <<endl;
	cout << "           88ooo   88       `8bd8'     88    88V8o 88 88           88   I8I   88    88       88    88ooo88         88    88oobY' 88    88 `8bo.      88   " <<endl;
	cout << "           88~~~   88         88       88    88 V8o88 88  ooo      Y8   I8I   88    88       88    88~~~88         88    88`8b   88    88   `Y8b.    88   " <<endl;
	cout << "           88      88booo.    88      .88.   88  V888 88. ~8~      `8b d8'8b d8'   .88.      88    88   88         88    88 `88. 88b  d88 db   8D    88   " <<endl;
	cout << "           YP      Y88888P    YP    Y888888P VP   V8P  Y888P        `8b8' `8d8'  Y888888P    YP    YP   YP         YP    88   YD ~Y8888P' `8888Y'    YP   " <<endl;
	cout << "                                                                                                                                                                   " <<endl;
	cout << "                                                                                                                                                                   " <<endl;
	cout << "             d88888b  .d88b.  d8888b.      d88888b d888888b db    db d88888b      d8888b. d88888b  .o88b.  .d8b.  d8888b. d88888b .d8888.                   " <<endl;
	cout << "             88'     .8P  Y8. 88  `8D      88'       `88'   88    88 88'          88  `8D 88'     d8P  Y8 d8' `8b 88  `8D 88'     88'  YP                   " <<endl;
	cout << "             88ooo   88    88 88oobY'      88ooo      88    Y8    8P 88ooooo      88   88 88ooooo 8P      88ooo88 88   88 88ooooo `8bo.                         YP " <<endl;
	cout << "             88~~~   88    88 88`8b        88~~~      88    `8b  d8' 88~~~~~      88   88 88~~~~~ 8b      88~~~88 88   88 88~~~~~   `Y8b.                    " <<endl;
	cout << "             88      `8b  d8' 88 `88.      88        .88.    `8bd8'  88.          88  .8D 88.     Y8b  d8 88   88 88  .8D 88.     db   8D      db db db db db " <<endl;
	cout << "             YP       `Y88P'  88   YD      YP      Y888888P    YP    Y88888P      Y8888D' Y88888P  `Y88P' YP   YP Y8888D' Y88888P `8888Y'      VP VP VP VP YP " <<endl;
	cout << "                                                                                                                                                                          " <<endl;
	cout << "                                                                                                                                                                          " <<endl;	

	cout<<"\t (a) Press 1 to Add new Passenger...                                                  "<<endl;
	cout<<"\t (b) Press 2 to Search a Passenger...                                                 "<<endl;
	cout<<"\t (c) Press 3 to Update the Data of the Passenger...                                   "<<endl;
	cout<<"\t (d) Press 4 to Delete a Passenger...                                                 "<<endl;
	cout<<"\t (e) Press 5 to Display all Passengers...                                             "<<endl;
	cout<<"\t (f) Press 6 to Display all flights registered by a Passenger...                      "<<endl;
	cout<<"\t (g) Press 7 to Display all registered Passengers is a flight...                      "<<endl;
	cout<<"\t (h) Press 8 to Delete a flight...                                                    "<<endl;
	cout<<"\t (i) Press 0 to Go to back to the Main Menu/Logout...                                 "<<endl;
	cout<<"\n\t Enter the desired option: ";
	cin>>choice;
	cout<<endl;
	main();
			
	}
	else{
	cout<<"\n LOGGIN ERROR!!! \n Please check your UserAdmin name and password\n"<<endl;
	main();
	}	
}
//**********************************************************************************************************************************************************
void registrationadmin ()
	{
		string ruserIdadmin,remail,rpassword,rpass;
//system("cls"); //cai nay de mo qua tab moi.
	cout <<"                                                                                                                   " <<endl;
	cout <<"                .d8b.  d8888b. .88b  d88. d888888b d8b   db      .d8888. d888888b  d888b  d8b   db db    db d8888b." <<endl;
	cout <<"              d8' `8b 88  `8D 88'YbdP`88   `88'   888o  88      88'  YP   `88'   88' Y8b 888o  88 88    88 88  `8D" <<endl;
	cout <<"              88ooo88 88   88 88  88  88    88    88V8o 88      `8bo.      88    88      88V8o 88 88    88 88oodD'" <<endl;
	cout <<"              88~~~88 88   88 88  88  88    88    88 V8o88        `Y8b.    88    88  ooo 88 V8o88 88    88 88~~~  " <<endl;
	cout <<"               88   88 88  .8D 88  88  88   .88.   88  V888      db   8D   .88.   88. ~8~ 88  V888 88b  d88 88     " <<endl;
	cout <<"               YP   YP Y8888D' YP  YP  YP Y888888P VP   V8P      `8888Y' Y888888P  Y888P  VP   V8P ~Y8888P' 88     " <<endl;
	cout <<"                                                                                                                    " <<endl;
	cout <<"                                                                                                                     " <<endl;
	cout<<"\t\t\t-----Welcome to the Administrator Registration Portal---------\n\n\n"<<endl;
	cout<<"Enter your UserName to Register: ";
	cin>>ruserIdadmin;
	cout<<"Enter your Password to the Register: ";
	cin>>rpassword;
	ofstream f1("admin.txt", ios::app);
	f1<<ruserIdadmin<<' '<<rpassword<<' '<<endl;
	//system("cls");
	cout<<"\n\t\t\t Registration is successfull! \n";
	main();	
	}
//************************************************************************************************************************************************************************************
void login()
{
	cout <<"                                                                                                                                " <<endl;
	cout <<  "          .o88b. db    db .d8888. d888888b  .d88b.  .88b  d88. d88888b d8888b.      db       .d88b.   d888b  d888888b d8b   db" << endl;
	cout <<  "         d8P  Y8 88    88 88'  YP `~~88~~' .8P  Y8. 88'YbdP`88 88'     88  `8D      88      .8P  Y8. 88' Y8b   `88'   888o  88" << endl;
	cout <<  "         8P      88    88 `8bo.      88    88    88 88  88  88 88ooooo 88oobY'      88      88    88 88         88    88V8o 88" << endl;
	cout <<  "         8b      88    88   `Y8b.    88    88    88 88  88  88 88~~~~~ 88`8b        88      88    88 88  ooo    88    88 V8o88" << endl;
	cout <<  "         Y8b  d8 88b  d88 db   8D    88    `8b  d8' 88  88  88 88.     88 `88.      88booo. `8b  d8' 88. ~8~   .88.   88  V888" << endl;
	cout <<  "          `Y88P' ~Y8888P' `8888Y'    YP     `Y88P'  YP  YP  YP Y88888P 88   YD      Y88888P  `Y88P'   Y888P  Y888888P VP   V8P" << endl;
	cout <<"                                                                                                                                " <<endl; 
    string remail, email, rpassword, id, pass, rphonenumber, raddress, rage, pw;
    bool found = false;
    //system("cls");
    cout << "Please enter the username and password!!!\n" << endl;
    cout << "Enter the Email to login: ";
    cin >> email;
    cout << "Enter the password: ";
    cin >> pw;

    ifstream input("records.txt");

    while (input >> id >> remail >> pass >> rphonenumber >> raddress >> rage)
    {
        if (email == remail && pw == pass)
        {
            found = true;
            break;
        }
    }
    input.close();

    if (found)
    {
        //system("cls");
        cout << "Welcome! You are logged in." << endl;

        int choice;
        cout << "For further proceedings, enter a value from below..." << endl;
        cout << "\t (a) Press 1 to Book a Flight...                                          " << endl;
        cout << "\t (b) Press 2 to Update your Data...                                       " << endl;
        cout << "\t (c) Press 3 to Delete your account...                                    " << endl;
        cout << "\t (d) Press 4 to Display Flight Schedule...                                " << endl;
        cout << "\t (e) Press 5 to Cancel a Flight...                                        " << endl;
        cout << "\t (f) Press 6 to Display all Flights registered by...                      " << endl;
        cout << "\n\t Enter the desired option: ";
        cin >> choice;
		switch(choice)
		{
		case 1:
			bookFlight();
			break;
		case 2:
			editUserInfo();
			break;
		case 3:
			deleteAccount();
			break;
//		case 4:
//			displaySchedule();
//			break;
//		case 5:
//			cancelFlight();
//			break;
//		case 6:
//			displayFlightRegister();
//			break;
			main();
		}
    }
    else
    {
        cout << "Sorry, the email and password you entered do not match any records." << endl;
    }
}
	
//**************************************************************************************************************************************************************************************	
void registration()
{
    string ruserId, remail, rpassword, rphonenumber, raddress, rage, rid, rmail, rphone, raddr, ra, rpass;
    bool emailExists = false;
//system("cls"); //cai nay de mo qua tab moi.
	cout <<"                                                                                                                                                 " <<endl;
	cout <<"                     .o88b. db    db .d8888. d888888b  .d88b.  .88b  d88. d88888b d8888b.      .d8888. d888888b  d888b  d8b   db db    db d8888b." <<endl;
	cout <<"                    d8P  Y8 88    88 88'  YP `~~88~~' .8P  Y8. 88'YbdP`88 88'     88  `8D      88'  YP   `88'   88' Y8b 888o  88 88    88 88  `8D" <<endl;
	cout <<"                    8P      88    88 `8bo.      88    88    88 88  88  88 88ooooo 88oobY'      `8bo.      88    88      88V8o 88 88    88 88oodD'" <<endl;
	cout <<"                    8b      88    88   `Y8b.    88    88    88 88  88  88 88~~~~~ 88`8b          `Y8b.    88    88  ooo 88 V8o88 88    88 88~~~  " <<endl;
	cout <<"                    Y8b  d8 88b  d88 db   8D    88    `8b  d8' 88  88  88 88.     88 `88.      db   8D   .88.   88. ~8~ 88  V888 88b  d88 88     " <<endl;
	cout <<"                     `Y88P' ~Y8888P' `8888Y'    YP     `Y88P'  YP  YP  YP Y88888P 88   YD      `8888Y' Y888888P  Y888P  VP   V8P ~Y8888P' 88     " <<endl;
	cout <<"                                                                                                                                                 " <<endl;
	cout <<"                                                                                                                                                 " <<endl;
    cout << "\t\t\t-----Welcome to the Customer Registration Portal---------\n\n\n"
         << endl;
    cout << "Enter your Username: ";
    cin >> ruserId;

    ifstream input("records.txt");
    while (input >> rid >> rmail >> rpass >> rphone >> raddr >> ra)
    {
        if (rmail == remail)
        {
            emailExists = true;
            break;
        }
    }
    input.close();

    if (emailExists)
    {
        cout << "Error: This email is already registered." << endl; 
        return;
    }

    cout << "Enter your Email address: ";
    cin >> remail;

    cout << "Enter your Password: ";
    cin >> rpassword;
    // Add password validation here (e.g. minimum length)

    cout << "Enter your Phone number: ";
    cin >> rphonenumber;

    cout << "Enter your address: ";
    cin >> raddress;

    cout << "Enter your age: ";
    cin >> rage;

    ofstream f1("records.txt", ios::app);
    f1 << ruserId << ' ' << remail << ' ' << rpassword << ' ' << rphonenumber << ' ' << raddress << ' ' << rage << endl;
    system("cls");
    cout << "\n\t\t\t Registration is successfull! \n";
    main();
}
//******************************************************************************************************************************************************************************************
class Flight {
public:
int num;
std::string flightSchedule;
std::string flightNumber;
std::string availableSeats;
std::string from;
std::string to;
std::string arrivalTime;
std::string flightTime;
std::string gate;
std::string distance;
};

void bookFlight() {
	cout <<"                                                                                            " <<endl;	
    cout <<"    d8888b.  .d88b.   .d88b.  db   dD      d88888b db      d888888b  d888b  db   db d888888b" << endl;
    cout <<"    88  `8D .8P  Y8. .8P  Y8. 88 ,8P'      88'     88        `88'   88' Y8b 88   88 `~~88~~'" << endl;
    cout <<"    88oooY' 88    88 88    88 88,8P        88ooo   88         88    88      88ooo88    88   " << endl;
    cout <<"    88~~~b. 88    88 88    88 88`8b        88~~~   88         88    88  ooo 88~~~88    88   " << endl;
    cout <<"    88   8D `8b  d8' `8b  d8' 88 `88.      88      88booo.   .88.   88. ~8~ 88   88    88   " << endl;
    cout <<"    Y8888P'  `Y88P'   `Y88P'  YP   YD      YP      Y88888P Y888888P  Y888P  YP   YP    YP   " << endl;
    cout <<"                                                                                            " <<endl;
std::ifstream inFile("flights.txt");
std::vector<Flight> flights;

int num;
std::string flightSchedule;
std::string flightNumber;
std::string availableSeats;
std::string from;
std::string to;
std::string arrivalTime;
std::string flightTime;
std::string gate;
std::string distance;

while (inFile >> num >> flightSchedule >> flightNumber >> availableSeats >> from >> to >> arrivalTime >> flightTime >> gate >> distance) {
flights.push_back({num, flightSchedule, flightNumber, availableSeats, from, to, arrivalTime, flightTime, gate, distance});
}

std::cout<< "+----+----------------+-----------+--------------+-------+-----+-------+----------+-------------+\n";
std::cout<<"| Num | Flight Schedule| Flight No | Available Seats| From | To | Arrival Time | FlightTime |Gate| Distance |\n";
std::cout<<"+-----+----------------+-----------+--------------+-------+-----+-------+----------+-------------+\n";

for (std::vector<Flight>::const_iterator it = flights.begin(); it != flights.end(); ++it) {
const Flight& flight = *it;
std::cout << "|" << flight.num << "|" << flight.flightSchedule << "|" << flight.flightNumber << "|" << flight.availableSeats << "|" << flight.from << "|" << flight.to << "|" << flight.arrivalTime << "|" << flight.flightTime << "|" << flight.gate << "|" << flight.distance << std::endl;
}
}
//*********************************************************************************************************************************************************************************************************************************************************************************

void editUserInfo()
{ 
	cout <<"                                                                                             " <<endl;
	cout <<"                    d88888b d8888b. d888888b d888888b      d888888b d8b   db d88888b  .d88b. " <<endl;
	cout <<"                    88'     88  `8D   `88'   `~~88~~'        `88'   888o  88 88'     .8P  Y8." <<endl;
	cout <<"                    88ooooo 88   88    88       88            88    88V8o 88 88ooo   88    88" <<endl;
	cout <<"                    88~~~~~ 88   88    88       88            88    88 V8o88 88~~~   88    88" <<endl;
	cout <<"                    88.     88  .8D   .88.      88           .88.   88  V888 88      `8b  d8'" <<endl;
	cout <<"                    Y88888P Y8888D' Y888888P    YP         Y888888P VP   V8P YP       `Y88P' " <<endl;
	cout <<"                                                                                             " <<endl;
	string ruserId, remail, rphonenumber, raddress, rage, rid, rmail, rphone, raddr, ra;
    bool emailExists = false;
    cout << "Enter the new name of the Passenger: ";
    cin >> ruserId;

    ifstream input("records.txt");
    ifstream output("update.txt");
    while (input >> rid >> rmail >> rphone >> raddr >> ra)
    {
        if (rmail == remail)
        {
            emailExists = true;
            break;
        }
    }
    input.close();

    if (emailExists)
    {
        cout << "Error: This email is already registered." << endl; 
        return;
    }

    cout << "Enter the new email address of Passenger: ";
    cin >> remail;

    cout << "Enter the new phone number of Passenger: ";
    cin >> rphonenumber;

    cout << "Enter the new address of Passenger: ";
    cin >> raddress;

    cout << "Enter the new age of Passenger: ";
    cin >> rage;

    ofstream f1("records.txt", ios::app);
    f1 << ruserId << ' ' << remail << ' ' << ' ' << rphonenumber << ' ' << raddress << ' ' << rage << endl;
    system("cls");
    cout << "\n\t\t\t Update data is successfull! \n";
    main();
	
	class Update {
	public:
	int num;
	std::string userID;
	std::string passengerName;
	std::string age;
	std::string emailID;
	std::string homeAddress;
	std::string phoneNumber;
};
	std::ifstream inFile("update.txt");
	int update;
	int num;
	std::string userID;
	std::string passengerName;
	std::string age;
	std::string emailID;
	std::string homeAddress;
	std::string phoneNumber;
	while (inFile >> num >> userID >> passengerName >> age >> emailID >> homeAddress >> phoneNumber) {
	//update.push_back({num, userID, passengerName, age, emailID, homeAddress, phoneNumber});
}

std::cout<< "+----+----------------+-----------+--------------+-------+-----+-------+----+\n";
std::cout<<"| Num | UserID | Passenger Names | Age | EmailID | HomeAddress | PhoneNumber |\n";
std::cout<<"+-----+----------------+-----------+--------------+-------+-----+-------+----+\n";
//std::cout << "|" << update.num << "|" << update.userID << "|" << update.passengerName << "|" << update.age << "|" << update.emailID << "|" << update.homeAddress << "|" << update.phoneNumber << std::endl;	
}
//***********************************************************************************************************************************************************************************
void deleteAccount()
{
	
}
	






	
