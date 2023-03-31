# ATM-Management-System
print("-------------Welcome to SBI ATM-----------------")
print("Select the service that you want to proceed:")
Services='''             1.QR CODE BANKING
             2.YONO BANKING
             3.CARD BANKING'''
print(Services)
service=["QR CODE BANKING,YONO BANKING,CARD BANKING"]
print(service)
card=['debit','credit','ministatement','exist']
yono=['debit','exist']
qr=['debit','credit','exist']
AccountBalance=4000
inputt=input('''PRESS "QR" FOR QR BANKING, PRESS "YONO" FOR YONO BANKING, PRESS "CARD" FOR CARD BANKING:''')
if inputt=='QR':
    pin=int(input("enter your 5 digit qr pin to proceed:"))
    if pin==93810:
        print(qr)
        select=input("select the option:")
        if select=='debit':
            amt=int(input("enter the amount:"))
            AccountBalance-=amt
            print("Your Remaining Balance:",AccountBalance)
        elif select=='credit':
            amt=int(input("enter the amount:"))
            AccountBalance+=amt
            print("Your Remaining Balance:",AccountBalance)
        elif select=='exist':
            print("Thank you for reaching us! Logged out successfully. Have a nice day")
        else:
            print("you have selected incorrect option. Try again!")
    else:
        print("You entered incorrect pin! Try Again!")
elif inputt=='YONO':
    ypin=int(input("Please enter your 6 digit yono password:"))
    if ypin==938100:
        print(yono)
        yselect=input("select the option:")
        if yselect=='debit':
            yamt=int(input("enter the amount:"))
            AccountBalance-=yamt
            print("Your Remaining Balance:", AccountBalance)
            print("Thank you for reaching us! Have a nice day!")
        elif yselect=='exist':
            print("logged out suxxessfully!")
            print("Thank you for reaching us! Have a nice day!")
        else:
            print("Incorrect option.Try Again.")
    else:
        print("Incorrect Pin! Try Again.")
elif inputt=='CARD':
    cpin=int(input("enter your 4 digit card pin:"))
    if cpin==9381:
        print(card)
        cselect=input("select the option to proceed:")
        if cselect=='debit':
            camt=int(input("enter the amount:"))
            AccountBalance-=camt
            print("Your Remaining Balance:", AccountBalance)
            print("Thank you for reaching us! Have a nice day!")
        elif cselect=='credit':
            camt=int(input("enter the amount:"))
            AccountBalance+=camt
            print("Your Remaining Balance:", AccountBalance)
            print("Thank you for reaching us! Have a nice day!")
        elif cselect=='ministatement':
            print("Your Balance:", AccountBalance)
            print("Thank you for reaching us! Have a nice day!")
        elif cselect=='exist':
            print("Loggedout successfully")
            print("Thank you for reaching us! Have a nice day!")
        else:
            print("Incorrect option! Try again.")
    else:
        print("Incorrect pin! Please Try Again.")
else:
    print("Invalid Option!")
    print("PLEASE TRY AGAIN!")



