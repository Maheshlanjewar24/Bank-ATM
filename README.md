# Bank-ATM
print('Welcome to python.hub Bank ATM')

restart=('y')


chances = 3


balance = 999.12


while chances >= 0:


   pin = int(input('Please Enter You 4 Digit Pin : '))


   if pin == (1234):


       print('You Entered You Pin Correctly')


       print('Please Press 1 For Your Balance')


       print('Please Press 2 To make A Withdrawl')


       print('Please Press 3 To Pay in')


       print('Please press 4 To Return Card\n')


       while restart not in ('n', 'No', 'no', 'N'):


           print('Please Press 1 For Your Balance')


           print('Please Press 2 To make A Withdrawl')


           print('Please Press 3 To Pay in')


           print('Please press 4 To Return Card')


           option = int(input('What Would you like to choose? : '))


           if option == 1:


               print('Your Balance is Rs',balance)


               restart = input('Would You like to go back? ')


               if restart in ('n', 'No', 'no', 'N'):


                   print('Thank You')


                   break


           elif option == 2:


               option2 = 'y'


               withdrawl = float(input('How Much Would you like to withdraw? 10,20,40,60,80,100 for other enter 1: '))


               if withdrawl in [10,20,40,60,100]:


                      balance = balance - withdrawl


                      print('\nYour Balance is now Rs',balance)


                      restart = input('Would You like to go back? ')


                      if restart in ('n', 'No', 'no', 'N'):


                          print('Thank You')


                          break


                      elif withdrawl != [10,20,40,60,100]:


                       print('Invalid Amount, PLease Re-try\n')


                       restart = 'y'


                      elif withdrawl == 1:


                       withdrawl = float(input('Please Enter Desired Amount: '))


           elif option == 3:


                Pay_in = float(input('How Much Would You Like To Pay In? '))


                balance = balance + Pay_in


                print('\nYou Balance is now Rs',balance)


                restart = input('Would You like to go back? ')


                if restart in ('n', 'No', 'no', 'N'):


                    print('Thank You')


                    break


           elif option == 4:


                print('Please wait while your card is returned......\n')


                print('Thank You for you service')


                break


           else:


                print('Please Enter a correct number. \n')


                restart = ('y')


   elif pin != ('1234'):


       print('Incorrect Password')


       chances = chances - 1


       if chances == 0:


           print('\nNo more tries')


           break

