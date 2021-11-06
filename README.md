# Try to write a code for ATM Machine interface .

print("\nWelcome to AK Bank ATM\n")
restart = ('y') 
chances = 3
balance = 675.23

while chances >= 0:
    pin = int(input("Please Enter Your 4 Digit Password : "))
    if pin == (0000):
        print("Your pin is correct\n")
        while restart  not in ('n','NO','no','N'):
            print("Press 1 for  Your Banlance : ")
            print("Press 2 for Withdrowl Money : ")
            print("Press 3 for Pay_in : ")
            print("Press 4 for Return Card :\n ")
            option = int(input("What would you like to choose : "))
            if option ==1:
                print("Your Account balance is ", balance,"\n")
                restart = input("Do you want to go back ? : ")
                if restart in ('n','NO','no','N'):
                    print (" Thank you ")
                    break
            elif option ==2:
                option2 = ('y')
                withdrowl = float (input("Please Select your amount :- \n (10 or 20 or 30 or 40 or 50 or 60 or 70 or 80 or 90 or 100) :- "))
                if withdrowl in [10,20,30,40,50,60,70,80,90,100]:
                    balance = balance - withdrowl 
                    print("\n Your Balance is now : ",balance,"\n")
                    restart = input("Would you want to go back ")
                    if restart in ('n','NO','no','N'):
                        print("Thank you ")
                        break
                elif withdrowl != [10,20,30,40,50,60,70,80,90,100]:
                    print("Invalid Amount , Please Re-try \n")
                    restart = ('y')
                elif withdrowl ==1:
                    withdrowl = float(input("Please Enter Desired Amount : "))

            elif option ==3:
                pay_in = float(input("Amount to pay_in ? : "))
                balance = balance + pay_in
                print("\n Your balance is now ",balance )
                restart = input("would you like t g Back ? ")
                if restart in ('n','NO','no','N'):
                    print("Thank you ")
                    break
            
            elif option ==4:
                print("Please wait your Card is Removing : ")
                print("Thank you for you service ")
                break 
            else :
                print("Please Enter a correct no. \n")
                restart =('y')
    elif pin !=('1234') :
        print("Incorrect password ")
        chances = chances -1
        if chances ==0:
            print("\n No more tries \n Thank you for visiting our Bank")
            break
            
            
            
                        #   By Akshay Bhardwaj
