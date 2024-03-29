# EmManaSystem
1.	Main program:
In the main program, we declare 4 variables, including i (the number of employees), ans (the answer to choosing an option), m (the answer to asking for entering more in option 1), and finally, pointers that point to the addresses of arrays that include the data of each employee.
Next, we use "Do... while looping" to ask the users to enter their choice at least once before asking for another choice. After that, we use "switch looping," which includes six options from 0 to 5 and a default option (for options that differ from 0 to 5), to determine the option of the user. If the option selected by the user differs from 0 to 5, the program will notify the user that it is an "invalid option."

2.	Option 1: 
For option 1, we use "do…while looping", as the fundamental we discussed above, to enter the employee’s data at least once before asking the user to enter more. First, we need to initialize the value of "flag", which shows the state of the searching ID, to 0 before checking if it already exists or not, and a pointer e[i] to store the data of ith employee. Secondly, the program will call the function "enter_em" to enter the name, ID, designation, department, and salary of the user. After that, we use "for looping" to check the ID with a counter "l". The value of "l" runs from 1 to the current entering employee (for instance, the nth employee) to compare the ID of the nth employee to the (n – l)th employee by using the built-in function “strcmp”. If the ID already exists that means there are no differences between 2 compared IDs so the value of strcmp will be 0 and the state of the flag will be equal to 1 and break the loop. After that, the program will check the value of the flag; if the flag is different from 0, it means the ID already exists, so the data will not be received, and the number of employees will remain the same. Finally, the program will ask the user to enter more. If the user presses ‘Y’, the new loop will start with the value of the flag reset to 0 and the number of employees ‘i’ increase by 1. If the user presses ‘N’ the program will return to entering the option session.

3.	Option 2:
For option 2, we use the function "display_all" that takes the pointer that points to the address of the data of employees and the value "i"—the number of employees. 
In the function "display_all", we use "for looping" with a counter that runs from 0 to the number of employees (in this function, we declare this variable as "a") to print the data from the 0th to a-th employee.

4.	Option 3:
For option 3,  we use the function "edit_em" to edit the information of a certain employee.
In function “edit_em”. Firstly, the function will take the pointer that points to the address of data of employees and the number of employees (in this function, we declare this variable as “a”). We also declare a flag (show the state of the searching ID) and pos (show the position of the searched ID) . Then the ID of the employee will be provided by the user, and we use a “for looping” run from 0 to “a” to compare the entered ID with all IDs of employees by the built-in function "strcmp" to find the ID that needs to be edited. If the ID is found, it results in the value of flag = 1 and pos = i (position of entered ID). If flag = 1 (means the ID is found), the user will enter the data of that employee again; however, the ID will not be allowed to change; it must remain the same. If lag = 0, the program will notify that “ID is not found” and the user will have to enter the option again.

5.	 Option 4:
For option 3, we use the function "cal_payment" to calculate the payment of a certain employee. 
In the function "cal_payment", the function will take the pointer that points to the address of data of employees and the number of employees (in this function, we declare this variable as “a”). Firstly, the ID of the employee will be provided by the user, and the program will use the built-in function "strcmp" in a “for looping” that runs from 0 to the last employee to find the ID that needs to calculate the payment. If the ID is found, the program will give the value of pos = i (the position of the employee needs to calculate payment) and flag = 1 (to notice that the ID is found). 
If flag = 1 (means that ID found) then the payment of the employee at position “i” will be calculated based on these 3 conditions:
•	If the salary in 1 year is over $15000 will be charged for 10% tax: we will take the salary multiplied by 90% to find the payment if the salary is > $15000.
•	If the salary in 1 year is over $25000, the extra charge of 5% for the redundant amount: in this case, the salary of the employee still be charged 10% tax as same as the first case, but the amount of money of salary which greater than $25000 will be extra charged 5%. For example, if the salary of an employee is $30000 per year, the tax will be $3000. Then the salary will be compared to $25000 by taking $30000 - $25000 = $5000. This difference will be an extra charge of 5%, $5000 x 5% = $250. Finally, the payment will be $30000 - $3000 - $250 = $26750
•	If the salary in 1 year is less than $15000, the salary will not be charged any tax, so the payment will equal to salary multiplied by 12 months.

 	If flag = 0 (means that ID is not found), the program will notify “ID is not found” and the user will enter the option again.
6.	Option 5:
 	For option 5, we assign the value of i (number of employees) equal to the result of the function "delete_em" to do both tasks, deleting an employee and updating the total number of employees.
 		In the function "delete_em", it takes the pointer that points to the address of the data of employees, the original number of employees (in this function, we declare this variable as “a”), and returns the number of employees after deleting. We also declare some variables: pos - to show the position of the entered ID; flag - to show the state of searching for ID. About the algorithm, we use "for looping" with a counter "i," which runs from 0 to the total number of employees “a”, and the built-in function “strcmp” to compare the entered ID to the ID of the 1st, 2nd,..., a-th employee. If the ID is found, the value of the flag is 1 (that means the ID is found), and the value of pos is the order i-th of the entered ID. After that, the value of the name, ID, designation, department, and salary of the entered employee will be replaced by the data of the next employee. Finally, the total number of employees will decrease by 1. If the flag = 0 ( that means ID is not found), the program will notify the user that "ID is not found", all data will be kept as original and the value of “a”, number of employees, will still remain the same.

7. Result:
   
![image](https://github.com/doanminh2203/Employee-Management-System/assets/153622274/1c9853a1-d40d-432e-a2f1-be1f5379ef9d)
![image](https://github.com/doanminh2203/Employee-Management-System/assets/153622274/d5451f99-ca74-41c0-8cc7-72265778fd5c)
![image](https://github.com/doanminh2203/Employee-Management-System/assets/153622274/5af5f66a-37c4-495f-88a0-6fbe6b60dc74)


