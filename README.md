# OOP.PROJECT
#include<iostream>
#include<string>
#include<map>
#include<cstdlib>
#include<fstream>
using namespace std; 
class Login{
	private:
		string username;
		string password;
	public:
		  Login(string u, string p)
	{
	 username=u; 
	 password=p;
	}	
	
	 	bool validation()

	 	{
	 	string un,pw;
		ifstream file("temp.txt");
        if (file.is_open())
	{
        getline(file, un);
        getline(file, pw);
        file.close();
        if (username == un && password == pw) {
               return true;
           }
       }
		else
		{
			cout<<"Invalid Password!";
		}
        return false;
    }

}; 

class Inventory
{
	map<string,int> items;
	int quantity;
	public:
	 Inventory(){
	 	items["Latte"] = 100;
        items["Cookie"] = 150;
        items["Molten Lava"] = 80;
        items["Hot Chocolate"] = 120;
        items["Milk"] = 200;
        items["Water"] = 300;
        items["Club Sandwich"] = 100;
        items["Grilled Sandwich"] = 120;
        items["Espresso"] = 90;
        items["Mocha"] = 100;
        items["Tea"] = 150;
        items["French Fries"] = 200;
        items["Black Coffee"] = 100;
        items["Coffee"] = 150;
        items["Cappuccino"] = 120;
        items["Green Tea"] = 150;
        items["Pastries"] = 180;
        items["Soup"] = 150;
        items["Pina Colada"] = 80;
        items["Mint Margarita"] = 90;
    
	}
	
    	 void updateInventory(string item, int quantity) {
        if (items[item] < 0 && items[item] >= quantity) { 
            items[item] -= quantity; 
            cout << "			Order successful! Enjoy your " << item << "." << endl;
        } else {
        	cout<<" ";
            cout <<"\n			Sorry,it's out of stock. " << endl;
        }
    }

        void Bill(string item, int quantity){
//        	 if (items[item] < quantity) {
//            cout << "\n			Sorry,it's out of stock. " << endl;
            
    //}
        	cout<<" ";
            if(item=="latte" || item=="Latte"){
            	cout<<"\n 			Your order for "<<quantity<<" Latte is confirmed.\n";            	
			   
				cout<<"			Your total bill is Rs "<<quantity*450<<" .";
}
        
            else  if(item=="Molten lava" || item=="molten lava"){
        		cout<<"\n			 Your order for "<<quantity<<" Molten Lava is confirmed.\n";
				cout<<"				Your total bill is Rs "<<quantity*550<<" .";
				
			}
			   else if(item == "Cookie" || item == "cookie"){
            cout<<"\n 			Your order for "<<quantity<<" Cookie is confirmed.\n";            	

            cout<<"\n 		Your total bill is Rs"<<quantity*300<<".";
			        }
        
			    else if(item == "Hot Chocolate" || item == "hot chocolate"){
			    	cout<<"\n 			Your order for "<<quantity<<" Hot Chocolate is confirmed.\n";

            		cout<<"			Your total bill is Rs " << quantity * 480 << " .";
        }
        		else if(item == "Milk" || item == "milk"){
                    cout<<"\n 			Your order for "<<quantity<<" milk is confirmed.\n";
			        cout << "			Your total bill is Rs " << quantity*120 << " .";
        }
       			else if(item == "Water" || item == "water"){
        			cout<<"\n 		Your order for "<<quantity<<" Water is confirmed.\n";
            		cout << "\n			Your total bill is Rs " << quantity * 100 << " .";
        }
       			else if(item == "Club Sandwich" || item == "club sandwich"){
        			cout<<"\n 			Your order for "<<quantity<<" Club Sandwich is confirmed.\n";

            		cout << "			Your total bill is Rs " << quantity * 420 << " .";
        }
        		else if(item == "Grilled Sandwich" || item == "grilled sandwich"){
       		    	cout<<"\n 			Your order for "<<quantity<<" Grilled Sandwich is confirmed.\n";
            		cout << "			Your total bill is Rs " << quantity * 450 << " .";
        }
        else if(item == "Espresso" || item == "espresso"){
            		cout<<"\n 			Your order for "<<quantity<<" Espresso is confirmed.\n";
					 cout << "			Your total bill is Rs " << quantity * 400 << " .";
        }
        else if(item == "Mocha" || item == "mocha"){
        	
            cout << "\n				Your order for " << quantity << " Mocha is confirmed.\n";
            cout << "			Your total bill is Rs " << quantity * 400 << " .";
        }
        else if(item == "Tea" || item == "tea"){
        				    	cout<<"\n 			Your order for "<<quantity<<" Tea is confirmed.\n";

            cout << "\n				Your order for " << quantity << " Tea is confirmed.\n";
            cout << "			Your total bill is Rs " << quantity * 200 << " .";
        }
        else if(item == "French Fries" || item == "french fries"){
        	
            cout << "\n				Your order for " << quantity << " French Fries is confirmed.\n";
            cout << "		Your total bill is Rs " << quantity * 380 << " .";
        }
        
        else if(item == "Black Coffee" || item == "black coffee"){

            cout << "\n				Your order for " << quantity << " Black Coffee is confirmed.\n";
            cout << "			Your total bill is Rs " << quantity * 400 << " .";
        }
        else if(item == "Coffee" || item == "coffee"){

            cout << "			Your order for " << quantity << " Coffee is confirmed.\n";
            cout << "\n			Your total bill is Rs " << quantity * 450 << " .";
        }
        
        else if(item == "Cappuccino" || item == "cappuccino"){
        	cout<<"\n 			Your order for "<<quantity<<" Cappuccino is confirmed.\n";
            cout << "\n			Your total bill is Rs " << quantity * 400 << " .";
        }
        
        else if(item == "Green Tea" || item == "green tea"){
        	cout<<"\n	 		Your order for "<<quantity<<" Green tea is confirmed.\n";
            cout << "\n			Your total bill is Rs " << quantity * 200 << " .";
        }
        
        else if(item == "Pastries" || item == "pastries"){
        	
            cout << "\n				Your order for " << quantity << " Pastries is confirmed.\n";
            cout<<"\n			Your total bill is Rs " << quantity * 350 << " .";
        }
        
        else if(item == "Soup" || item == "soup"){
        	cout<<"\n 			Your order for "<<quantity<<" Soup is confirmed.\n";
            cout<<"\n			Your total bill is Rs " << quantity * 300 << " .";
        }
        
        else if(item == "Pina Colada" || item == "pina colada"){
            cout << "\n				Your order for " << quantity << " Pina Colada is confirmed.\n";
            cout<<"\n			Your total bill is Rs " << quantity * 600 << " .";
        }
        
        else if(item == "Mint Margarita" || item == "mint margarita"){
        		cout<<"\n 			Your order for "<<quantity<<" Mint Margarita is confirmed.\n";
	            cout<<"			Your total bill is Rs " << quantity * 600 << " .";
        } 
	}
	};

class Cafe //: public Inventory
{
	private:
		int quantity;
		Inventory& inv;
	public:
		 Cafe(Inventory& inventory) : inv(inventory) {} // constructor
		// functions
	void latte(){
		cout<<"\n			Enter the quantity of Latte:		";
		cin>>quantity;
		 inv.updateInventory("Latte", quantity);
        inv.Bill("Latte", quantity);
	//	cout<<"			Your total bill is Rs "<<quantity*450<<" .";
	}	
	void cookie(){
		cout<<"\n			Enter the quantity of cookie:		";
		cin>>quantity;
		inv.updateInventory("Cookie", quantity);
        inv.Bill("Cookie", quantity);

	//	cout << "			Your total bill is Rs " << quantity * 300 << "." ;
	}	
	void moltenLava()
	{
		cout<<"\n			Enter the quantity of Molten Lava :		";
		cin>>quantity;
	inv.updateInventory("Molten Lava", quantity);
        inv.Bill("Molten Lava", quantity);
	
	}	
	void hotChocolate()
	{
	cout<<"\n			Enter the quantity of hot chocolate:		";
		cin>>quantity;
				inv.updateInventory("Hot Chocolate", quantity);
		        inv.Bill("Hot Chocolate", quantity);
		
	}	
	void milk(){
	cout<<"\n			Enter the quantity of Milk:		";
		cin>>quantity;
			inv.updateInventory("Milk", quantity);
        inv.Bill("Milk", quantity);
			
	}
	void water(){
	cout<<"\n			Enter the quantity of water bottle:		";
		cin>>quantity;
				inv.updateInventory("Water", quantity);	
		 inv.Bill("Water", quantity);		
				}
	void Clubsandwich(){
	cout<<"\n			Enter the quantity of club sandwich:		";
		cin>>quantity;
		cout<<"\n 			Your order for "<<quantity<<" club sandwich is confirmed.\n";
		   cout << "\n			Your total bill is Rs " << quantity * 420 << ".";
		inv.updateInventory("Club Sandwich", quantity);
        inv.Bill("Club Sandwich", quantity);

	}
	void Grilledsandwich(){
	cout<<"\n			Enter the quantity of grilled sandwich:		";
		cin>>quantity;
			inv.updateInventory("Grilled Sandwich", quantity);
        inv.Bill("Grilled Sandwich", quantity);

	}
	 void espresso(){
	cout<<"\n			Enter the quantity of espresso:		";
		cin>>quantity;
			inv.updateInventory("Espresso", quantity);
		        inv.Bill("Espresso", quantity);
	
}
	void mocha(){
		cout<<"\n			Enter the quantity of mocha:		";
		cin>>quantity;
			inv.updateInventory("Mocha", quantity);
		        inv.Bill("Mocha", quantity);
	
}
	void tea(){
	cout<<"\n			Enter the quantity of tea:		";
		cin>>quantity;
				inv.updateInventory("Tea", quantity);
		        inv.Bill("Tea", quantity);
		

	}
	void frenchFries(){
	cout<<"\n			Enter the quantity of french fries:		";
		cin>>quantity;
				inv.updateInventory("French fries", quantity);


	}
	void blackCoffee(){
			cout<<"	\n		Enter the quantity of Black coffee:		";
		cin>>quantity;
				inv.updateInventory("Black Coffee", quantity);
        inv.Bill("Black Coffee", quantity);

	}
	void Coffee(){
			cout<<"\n			Enter the quantity of coffee:		";
		cin>>quantity;
				inv.updateInventory("Coffee", quantity);
			        inv.Bill("Coffee", quantity);
	

	}
	void cappuccino(){
			cout<<"			Enter the quantity of cappuccino:		";
		cin>>quantity; 
				inv.updateInventory("Cappuccino", quantity);
        inv.Bill("Cappuccino", quantity);

	}
	void Greentea(){
		cout<<"\n			Enter the quantity of green tea:		";
		cin>>quantity;
					inv.updateInventory("Green Tea", quantity);
        inv.Bill("Green Tea", quantity);

	}	
	void pastries(){
		cout<<"	\n		Enter the quantity of pastry:		";
		cin>>quantity;
					inv.updateInventory("Pastry", quantity);
        inv.Bill("Pastries", quantity);

	}		
	void soup(){
		cout<<"\n			Enter the quantity of soup:		";
		cin>>quantity;
				inv.updateInventory("Soup", quantity);
				inv.Bill("Soup",quantity);
			}
	void pinaColada(){
		cout<<"\n			Enter the quantity of pina colada:		";
		cin>>quantity; 
				inv.updateInventory("Pina Colada", quantity);
        inv.Bill("Pina Colada", quantity);

	}	
	void mintMargarita(){
		cout<<"\n			Enter the quantity of mint margarita:		";
		cin>>quantity;
				inv.updateInventory("Mint Margarita", quantity);
				 inv.Bill("Mint Margarita", quantity);

}
	void reorder(){
	string answer;
    string item;
    int quantity;
    cout<<"\n			Do You Want Anything Else?		 ";
    cin>>answer;
	if(answer=="Yes" || "yes"){
	
    cout<<"\n			Enter the item you want to reorder:  ";
    cin>>item;
    cout<<"\n			Enter the quantity: 	 ";
    cin>>quantity;
    inv.updateInventory(item, quantity); 
    inv.Bill(item,quantity);
}
	else {
		cout<<"\n		Enjoy Your Day Sir.";
	}
}

//	void DisplayBill() {l
//    inv.Bill();
//}

};
class Customer{
	string name;
	int no;
	int id;
	public:
		Customer() {}
    		Customer(string n, int i, int o) : name(n), id(i), no(o) {}
    		void Display(){
    			cout<<"\n		ENTER CUSTOMEER NAME	:	";
    			cin>>name;
    			cout<<"\n		ENTER CUSTOMER ID	:	";
    			cin>>id;
    			cout<<"\n		ENTER CONTACT NUMBER	:	";
    			cin>>no;
    			ofstream out("sample6.txt");
    			out<<name;
    			out<<no;
    			out<<id;
    			
			}
};
int main(){

	
	  string user="sadia";
	 	string pass="boss";
	 //	 string userS="salesman" ;
	 //	string passS="coffee";
	 	
	 	string ans;
	 	ofstream out ("login.txt");
	 	out<<user<<"\n"<<pass;

		string username,password;
		cout<<"Log In as Admin or Salesman : \n";
		cin>>ans;
		
	 	cout<<"username : "<<endl;
		cin>>username;
	 	cout<<"password : "<<endl;
		cin>>password;
	Login login(username, password);

    if (login.validation()) {
        cout << "Login successful!" << endl;
    } else {
        cout << "Incorrect username or password." << endl;
           return 1; 
    }
    Customer detail;
	detail.Display();
    Inventory inv;
    Cafe c(inv);
	int choice;
	int quantity;
	int item;
	//while (username==user && password==pass)
	//{
	  cout<<"******************************************************************************************************************************"<<endl;
    //  cout<<"*                             															*"<<endl;
     // cout<<"*                             															*"<<endl;
      //cout<<"*                             															*"<<endl;
      cout<<"\n								WELCOME TO COFFEE SHOP   								"<<endl;
  //    cout<<"*                             															*"<<endl;
     // cout<<"*                             															*"<<endl;
   //   cout<<"*                             															*"<<endl;
      cout<<"\n*****************************************************************************************************************************"<<endl;			

	cout<<"\n	\n						MENU \n";
	cout <<"1.  Latte		Rs.450\n";
cout <<"2.  Cookie		Rs.300\n";
cout <<"3.  Molten Lava		Rs.550\n";
cout <<"4.  Hot Chocolate	Rs.480\n";
cout <<"5.  Milk		Rs.120\n";
cout <<"6.  Water		Rs.100\n";
cout <<"7.  Club Sandwich	Rs.420\n";
cout <<"8.  Grilled Sandwich	Rs.450\n";
cout <<"9.  Espresso		Rs.400\n";
cout <<"10. Mocha		Rs.450\n";
cout <<"11. Tea			Rs.200\n";
cout <<"12. French Fries	Rs.380\n";
cout <<"13. Black Coffee	Rs.400\n";
cout <<"14. Coffee		Rs.450\n";
cout <<"15. Cappuccino		Rs.400\n";
cout <<"16. Green Tea		Rs.200\n";
cout <<"17. Pastries		Rs.350\n";
cout <<"18. Soup		Rs.300\n";
cout <<"19. Pina Colada		Rs.600\n";
cout <<"20. Mint Margarita	Rs.600\n";

    cout<<" \n 						Enter your order: 	"; 
    cin>>choice;
	switch (choice)
	 {
    case 1:
  //  	inv.updateInventory("Lattee",quantity);
        c.latte();
//		inv.Bill("Latte", quantity);
        break;
    case 2:
   // 	inv.updateInventory("Cookie",quantity);
        c.cookie();
//		inv.Bill("Cookie", quantity);
        break;
    case 3:
    //	inv.updateInventory("Molten Lava",quantity);
        c.moltenLava();
   //     inv.Bill("Molten Lava", quantity);

         // c.DisplayBill;
        break;
    case 4:
    //	inv.updateInventory("Hot Chocolate",quantity);
        c.hotChocolate();
	//	inv.Bill("Hot Chovolate", quantity);

        break;
    case 5:
  //  inv.updateInventory("Milk",quantity);	
        c.milk();
   //     inv.Bill("Milk", quantity);
        break;
    case 6:
   // 	inv.updateInventory("Water",quantity);
        c.water();
    //    inv.Bill("Water",quantity);
		break;
    case 7:
    //	inv.updateInventory("Club Sandwich",quantity);
        c.Clubsandwich();
	//	inv.Bill("Club Sandwich", quantity);
		break;
    case 8:
    //	inv.updateInventory("Grilled Sandwich",quantity);
        c.Grilledsandwich();
	//	inv.Bill("Grillled Sandwich", quantity);
		break;
    case 9:
    //	inv.updateInventory("Espresso",quantity);
        c.espresso();
		//inv.Bill("Espresso", quantity);
		break;
    case 10:
    //	inv.updateInventory("Mocha",quantity);
        c.mocha();
		//inv.Bill("Mocha", quantity);
		break;
    case 11:
    //	inv.updateInventory("Tea",quantity);
        c.tea();
        //inv.Bill("Tea", quantity);

		break;
    case 12:
    //	inv.updateInventory("French Fries",quantity);
        c.frenchFries();
		inv.Bill("French Fries", quantity);
		break;
    case 13:
    //	inv.updateInventory("Black Coffee",quantity);
        c.blackCoffee();
	//	inv.Bill("Black Coffee", quantity);
		break;
    case 14:
    //	inv.updateInventory("Coffee",quantity);
        c.Coffee();
//		inv.Bill("Coffee", quantity);
		break;
    case 15:
    	//inv.updateInventory("Green Tea",quantity);
        c.cappuccino();
		//inv.Bill(item, quantity);
		break;
    case 16:
    	//inv.updateInventory("Green Tea",quantity);
        c.Greentea();
	//	inv.Bill(item, quantity);
		break;
    case 17:
        //inv.updateInventory("Pastry",quantity);
        c.pastries();
//		inv.Bill(item, quantity);
		break;
    case 18:
   		//inv.updateInventory("Soup",quantity);
        c.soup();
	//	inv.Bill(item, quantity);
		break;
    case 19:
    	//inv.updateInventory("PinaColada",quantity);
        c.pinaColada();
	//	inv.Bill(item, quantity);
		break;
    case 20:
	        c.mintMargarita();
       // 	inv.Bill("Mint Margarita", quantity);
			break;
    default: 
		cout << "Invalid choice." << endl; 
		break;
}
	c.reorder();
	
		return 0;

}
