# logisim-lab
 
****System Description:****
The system simulates a washing machine, the machine has three different programs from which the user can choose one at a time. In order to operate the machine the user will have to enter money according to the program he wishes to operate.


****Functional specifications:****

 • The machine has a stock of components (softener, soap and that thing your wife likes and you don't remember what it's called).
 
 • The system will take an amount of money from the user
 
 • The user will be able to choose one of three programs, according to the user's choice. If the user has entered enough money, the system will update the stock in the machine, calculate the excess and start running the appropriate program.
 
 • Depending on the program selected, the system will run up to eight different machines (or some of them) for different periods of time.
 
 • The system will show the user how long it will take for the washing machine to completely finish the program.

**** Detailed planning process:*****

• Accepting and agreeing money from the user using three buttons.

• Returning surplus according to the plan selected by the user.

• Updating the machine's inventory

• Operating up to eight machines at different times according to the user's choice using pre-saved ROM memory.

![image](https://github.com/user-attachments/assets/d759056f-76f7-4e92-b30d-2326a91a0020)

********behind the curtain:********

![image](https://github.com/user-attachments/assets/054ef8da-0dbc-4ac2-a900-624816b6cea8)

Receiving money:

The Bank has three inputs connected to the MUX according to the amount entered into the register, the register is connected in feedback to the ADDER and thus the money that comes in can be summed.

The system is built so that each button press activates the CLOCK

![image](https://github.com/user-attachments/assets/ccaec9be-7c61-4daf-b5c8-22ef0c31ba74)

**Calculation of the surplus and authorization to operate the system:**

The Activator receives information from the bank about how much money enters the machine. As soon as the program is used, the system knows how to compare the amount of money in the bank to the price of the required program. Using the Subtractor, the system calculates the surplus and shows it.
Only if there is more money in the bank than the cost of the program will the system issue an authorization to operate.
Since every button press in the system activates the clock, we added registers to create a delay so that the user can see the system working.

![image](https://github.com/user-attachments/assets/3420b9ff-7f57-47d8-8106-cae32b1d4cfa)

**Receiving a work permit**, updating the inventory and running the program:

Only if a work permit is received does the system update the inventory according to the user's selection. With the help of MUX, the system knows which COUNTER to contact and remove from the inventory.
The system then sends a signal to run the appropriate program. The system is also able to fill the inventory.

![image](https://github.com/user-attachments/assets/203f985e-9357-43a2-86cd-c3cbdc06b489)

**Running a unique program according to the user's choice.**


According to the user's choice, an address in RAM is entered into the MUX. At each address, different time periods are entered for eight different timers that simulate different machines. So for each program there are different and unique working times for this program. In the output, you can see which machines are working and what the final working time of the system is.

![image](https://github.com/user-attachments/assets/c7275111-03c5-4fa3-be12-47e6d4133484)


