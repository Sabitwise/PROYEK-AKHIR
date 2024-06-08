#include<iostream> 
#include<vector>
#include<iomanip>
#include<string>

using namespace std; 

struct menuitem {
    string item; 
    int price;
};

menuitem menu[8]; 
vector<menuitem> pilihan; 

void tampilanmenu(){
    cout<<"| NO | PILIHAN                      | HARGA |" << endl;
    cout<<"|===========================================|" << endl;
    for(size_t i = 0; i < 8; i++){
        cout<<"| "<<setw(2)<<i+1<<" | "<<setw(30)<<menu[i].item<<" | "<<menu[i].price<<"K |"<<endl;
    }
    cout<<"|===========================================|"<<endl;
}

void menupilihan(int* nomoritem){
    if(*nomoritem >= 1 && *nomoritem <= 8){
        pilihan.push_back(menu[*nomoritem-1]); 
        cout<<menu[*nomoritem - 1].item<<" has been added"<<endl;
    } else {
        cout<<"Wrong items."<<endl; 
    }
}

void alltotal(){
    int total = 0; 
    for (const auto& item : pilihan){
        total += item.price; 
    }
    cout<<"Total pembelian: "<<total<<"K"<<endl; 
    int* uang = new int; 
    cout<<"Uang yang diserahkan [K]: "; 
        cin>>*uang; 
    cout<<"Kembalian: "<<*uang-total<<"K"<<endl; 
    cout<<"Thank you"<<endl;
    delete uang; // Free the allocated memory
}

int main(){
    int* item = new int; 
    int* itemselection = new int;

    menu[0] = {"NASI CAMPUR BALI", 75}; 
    menu[1] = {"CHICKEN BALLONTINE", 79}; 
    menu[2] = {"MUSHROOM PIZZA", 75}; 
    menu[3] = {"AGLIO OLIO", 42}; 
    menu[4] = {"ESPRESSO", 21}; 
    menu[5] = {"GREEN HILL TEA", 35}; 
    menu[6] = {"FRESH AUTUMN", 32}; 
    menu[7] = {"YAKULT STRAWBERRY", 40};

    cout<<"|===========================================|"<<endl;
    cout<<"| WELCOME TO PEOPLE's PLACE                 |"<<endl;
    cout<<"|===========================================|"<<endl;
    cout<<"| FOOD & BEVERAGES                          |"<<endl;
    cout<<"|===========================================|"<<endl;

    tampilanmenu(); 

    cout<<"Input how many items you want to order: "; 
        cin>>*item; 

    int itemSelections[*item];
    
    for(int i = 0; i < *item; i++){
        cout << i + 1 << ". "; 
        cin >> itemSelections[i];
    }
    
    for(int i = 0; i < *item; i++){
        menupilihan(&itemSelections[i]);
    }

    alltotal();

    delete item; 
    delete itemselection; 

    return 0;
}
