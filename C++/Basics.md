
- # cout<<" Hello World " << variable_name ;  
	 Is used to print output . Hello World 20 (assume variavlbe name to be 20)

- # NEW LINE :
	- \n inside the quotes is used to print a new line .
	- << endl ; is also used as a new line .

- # cin >> x >>y 
	 This is used to give input to variables named x and y . 

- # bits/stdc++.h 
	This includes all the libraries that we are going to use in cpp

- # getline(cin, variable_name) ;
	What this does is it gives the whole line as a input to the string .

- # " " double quotes are used to store string values whereas ' ' single quotes are used to store character values . 
	To declare string :
		string x = "MY NAME IS GAURAV " ; 
		char y = 'g' ;

- # IF ELSE STATEMENTS :
 if(condition1){
< code block>
}
else if(condition2){
< code block>
}
else{
< code block>
}
- #  SWITCH CASE :
switch(variable_to_be_compared){
case 1 :
	< code block>
	break ; 
case 2 :
	< code block>
	break ; 
case 3 :
	< code block>
	break ; 
default:
	< code block>
	break ;
}

Here the variable_to+be_compared is compared to 1,2,3 and whichever it matched to is executed .
Here the break statement is executed so that it gets out of the switch case and does not execute the next conditions .
	Also a default case is given in case none of the switch case is executed.

- # Strings :
String are basically the data types which store a collection of character . 

string x ;
cin >> x ;
cout << x ;

Input : Hello Gaurav
Output :Hello 

This is because the cin commands assigns the value of x only as the first word of the sentence .
To get the full line as input to x :
	string x ;
	getline(cin , x) ;
	cout<< x ;
	Output : Hello Gaurav

Here the string is also a collection of characters and has indexing similar to that of arrays .
So if i say :
		string x = 'Hello Gaurav' ; 
		cout << x[4] ;

		Output : o

- # Arrays :
	- Array is a continuous data type which stores similar kind of data . 
	- Its indexing starts from 0 and all the operations that chan be performed on a variable can b performed on a element of an array .
int a[3] = {1,4,6} ;
cout<< a[2] ;

Output : 6

- # For Loops :
 The for loop is used when you know how many times the loop needs to run .
 Here the condition is checked at the start of the loop and then the code is executed .

Syntax :
```
	// for (intialization ; condtion ; updation)
	for(int i = 1 ; i<=10 ; i = i+1 ){
	cout<<"Gaurav " ;
	}
```

Output : Here the code block is executed 10 times and the value of i cannot be printed outside of the loop because the scope of the i is just inside the loop . If i was declared out of the loop then the value that would've been printed would be 11 .


- # While Loop :
This loop  is used when we don't know how many times we want to run the loop for .
Here the initialisation takes place outside the loop and the incrementation is done at the end of the loop .

Syntax :
```
	int i = 1 ;
	while(i<5){
	cout<<"Gaurav";
	i = i + 1 ;
	}
```

Output : Here the code block is executed 4 times and the value of i if printed out of the loop would be 5 .

- # Do while loop :
Here the code is executed at least once as the condition is checked at the end of the do while loop .

Syntax :
```
	int i = 2 
	do{
	cout<< "Gaurav" ; 
	i = i + 1 
	}while(i<1);
```

Output : Here the do while loop would run for 1 time only and would print Gaurav once and then get out of the loop .


- # Functions :

	- Functions are blocks of code which repeat the same task again and again .
	- These blocks of code help to modularise the code and increase the readability .
	- There are mainly 4 types of functions :
		- Void - this function does not return anything 
		- Return  - this function returns a input to the code 
		- Parameterised - this function does not have a parameter ie it is independent of the input 
		- Non Parameterised - this function has a parameter and the function depends on the input .

	- Syntax 
```
		return_type function_name(Parameters){
		
		// code_block 
		
		return_type return_varibale ;
		}
```
		
```
		// make a function to calculate max of two numbers :

		int maxx(int a , int b ){
		if (a>=b) return a ;
		else retrun b ;
		}

		int main(){
		int num1 = 10 ;
		int num2 = 30 ;
		int c = maxx(num1,num2)
		cout<< "The Number bigger of the two are : " << c ;
		return 0 ;
		}
		
```
Output: 
The Number bigger of the two are : 30 

- ## Pass by value and Pass by reference :
		-___PASS BY VALUE___  :
		- Pass by value means that a copy of the variable is sent to the function ie the original variable is not changed rather its copy is changed  .
		- ___PASS BY REFERENCE___:
		- Pass by reference means that the address of the variable is sent to the function and so the actual variable is changed . 
		- To use pass by reference we use & symbol while giving the parameter to the function .
		- All the functions on default use pass by value only __ARRAYS___ use pass by reference as default .

Example : Pass by Value 
```
	int modify(int num1 ){
	num1 = num1 + 10 ;
	cout<<"Value inside the function is  : "<< num1 <<endl ;
	return num1 ;
	}

	int main(){
	int num1 = 10 ;
	modify(num1);
	cout <<"Value inside the main block is : "<< num1 ;
	return 0;
	}
```
Out put :
Value inside the function is 20
Value inside the main block is 10

Example : Pass by Reference : (Here we have used & to pass the address of the variable)
```
	int modify(int &num1 ){
	num1 = num1 + 10 ;
	cout<<"Value inside the function is  : "<< num1 <<endl ;
	return num1 ;
	}

	int main(){
	int num1 = 10 ;
	modify(num1);
	cout <<"Value inside the main block is : "<< num1 ;
	return 0;
	}

```
Out put :
Value inside the function is 20
Value inside the main block  is 20
