#include <iostream>
#include <stdlib.h>
#include <string>
#include <fstream>
#include <ctime>
#include <sys/types.h>
#include <sys/stat.h>
#include <cerrno>
using namespace std;


int main () {
	
	
	system("color 0");
	cout<<"\n\n";
	cout<<"  WELCOME TO FILE MANAGEMENT SYSTEM\n";
	system("pause");
	system("cls");
	
	
		
     string option;
     system("color 1f");
	 menu:
	 cout << endl;
	 
     cout << "            SIMPLE FILE MANAGEMENT SYSTEM    " << endl;
     
     cout << "          (1) -> Save to a file            " << endl;
     cout << "          (2) -> View file content         " << endl;
     cout << "          (3) -> Obtain file size          " << endl;
     cout << "          (4) -> File Details              " << endl;
     cout << "          (5) -> Clear the file            " << endl;
     cout << "          (6) -> Delete the file           " << endl;
     cout << "          (7) -> Exit Program              " << endl;
     
     cout << "\n          Enter Your Choice:	";
     getline(cin,option);
     
     
     if (option == "1") {
     	
       system("cls");
       system("color 0");
       string textToSave;
     
       cout << "          ENTER THE NAME YOU WANT TO SAVE   \n" ;	
      
       cout << "        HERE: ";
       getline(cin,textToSave);
       ofstream saveFile ("file.txt");
       saveFile << textToSave;
       cout << "" << endl<< endl<< endl<< endl<< endl<< endl; 
       saveFile.close(); 
       
       system("pause");
 		system("cls");
 					
		goto menu;
     }
     
     if(option == "2") {
     	  system("color 0");
     	  system("cls");
          ifstream loadFile;
          loadFile.open ("file.txt", ifstream::in);				
         
          cout << "             THE FILE CONTAINS THE STRING     x\n" ;	
          
          cout << "        ";
          while (loadFile.good()){
               cout << (char) loadFile.get();
          }
          cout << "" << endl<< endl<< endl<< endl<< endl<< endl; 
    	  loadFile.close();
    	  
    	  system("pause");
 		system("cls");
 					
		goto menu;
     }
     
      if (option == "3") {
     	
     	system("cls");
     	system("color f");
        streampos begin,end;
  		ifstream myfile ("file.txt", ios::binary);							
 		begin = myfile.tellg();
  		myfile.seekg (0, ios::end);
  		end = myfile.tellg();
 		myfile.close();
 		
        cout << "                    THE FILE SIZE IS          \n" ;
        
        cout << "\n\n\n\t\t\t";
  		cout << (end-begin) << " bytes.\n";
		cout << "" << endl<< endl<< endl<< endl<< endl;    
  		
  		system("pause");
 		system("cls");
 					
		goto menu;
     }
     
      if (option == "4") {
     	
     	system("cls");
        int argc; 
		char** argv ;
   		struct stat fileInfo;

   		if (stat("file.txt", &fileInfo) != 0) { 
   		  system("color 04");
   		  cout << "\n\n\n\n\n\n\n";
	   	  
          cout << "              ERROR     \n" ;	
         
          cout << "        ";
	      cout << "\n\n\n\n\n\n\n";
	      return 0;
   		}

		system("color 0");
		
   		cout << "     Size               : " << fileInfo.st_size <<"  bytes"<<'\n';     
   		cout << "     Drive letter saved : " << (char)(fileInfo.st_dev + 'A') << '\n';  
   		cout << "     Created            : " << std::ctime(&fileInfo.st_ctime);         
   		cout << "     Modified           : " << std::ctime(&fileInfo.st_mtime);         
   		
  		cout << "\n\n\n";
  		system("pause");
 		system("cls");
 					
		goto menu;
     }
     
     if (option == "5") {
     	system("color 0");
     	system("cls");
 		std::ofstream ofs ("file.txt", std::ios::out | std::ios::trunc); 
		cout << "\n\n\n\n"; 
 		
        cout << "FILE SUCCESSFULLY CLEARED\n" ;	
       
 		
 		system("pause");
 		system("cls");
 					
		goto menu;
     }
     
     if (option == "6") {
     	system("color 0");
     	system("cls");
    	std::remove("file.txt"); 									
    	cout << "\n\n\n\n"; 
 		
        cout << "FILE SUCCESSFULLY REMOVED\n" ;	
       
 		
 		system("pause");
 		system("cls");
 					
		goto menu;
     }
     
     if (option == "7") {
     	system("color 0");
     	system("cls");
 			cout<<"\n\n";
			
 		
 		system("pause");
 		return 0;
     }
     
     else;
     system("cls");
			cout<<"\n\n\n\n\n\n";
			cout<<"\t\t\tERROR\n";
			
				
			cout<<"\t\t\tPlease input a valid number.\n";
			cout<<"\t\t\tPress any key to go back to the Menu.\n\n\n\n\n\n\n";
				
			system("pause");
			system("cls");
			goto menu;
			
     
     system("pause");
	 return 0;
}
