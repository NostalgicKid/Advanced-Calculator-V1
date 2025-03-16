# Advanced_Calculator_Version_N_one

def calc_multiplication(x, y):
    return x * y

def calc_division(x,y):
    return x / y

def calc_addition(x,y):
    return x + y

def calc_subtraction(x,y):
    return x - y

# def calc_x_y(x,y):
#     x,y = int(input("\nEnter the value of X:\n")), int(input("\nEnter the value of Y:\n"))

print("Welcome to JahCulator\n")

def calc_condition_operations(calc_prompt, x, y):
    if calc_prompt.lower() == 'm':
        result = calc_multiplication(x,y)
    
    elif calc_prompt.lower() == 'd':
        result = calc_division(x,y)
    
    elif calc_prompt.lower() == 'a':
        result = calc_addition(x,y)

    elif calc_prompt.lower() == 's':
        result = calc_subtraction(x,y)
    
    print(f"\n\nResult: {result}\n\n")

def calc_main_one():
    calc_prompt_1 = input("What calculations would you like to do?\nM - Multiplication\nD - Division\nA - Addition\nS - Subtraction\n\n")
    # x,y = int(input("Enter the value of X:\n")), int(input("\nEnter the value of Y:\n"))
    if calc_prompt_1.lower() in ['m', 'd', 'a', 's']:
        x_1,y_1 = int(input("\n\nEnter the value of X:\n")), int(input("\nEnter the value of Y:\n"))
        calc_condition_operations(calc_prompt=calc_prompt_1, x=x_1,y=y_1)
    # def calc_x_y(x,y):
    #     x,y = int(input("\nEnter the value of X:\n")), int(input("\nEnter the value of Y:\n")

    else:
        while calc_prompt_1.lower() not in ['m', 'd', 'a', 's']:
            calc_prompt_1 = input("We can't calculate that with using this operation, Please enter ")
        
        if calc_prompt_1 in ['m', 'd', 'a', 's']:
            x_2,y_2 = int(input("\n\nEnter the value of X:\n")), int(input("\nEnter the value of Y:\n"))
            calc_condition_operations(calc_prompt=calc_prompt_1, x=x_2,y=y_2)

             # print(f"\n\nResult: {result}\n\n")

def main_two():
    calc_prompt_2 = input("Would you like to do any calculations?\nY - Yes\nN - No\n")
    if calc_prompt_2.lower() == 'y':
        calc_main()
    elif calc_prompt_2.lower() == 'n':
        print("Okay, Have a nice day!")
    else:
        calc_prompt_2 = input("What? Enter Yes or No\nY - Yes\nN - No\n\n")
        while calc_prompt_2.lower() not in ['y', 'n']:
            print(calc_prompt_2)
                    
        if calc_prompt_2.lower() == 'y':
            calc_main()
        
        elif calc_prompt_2.lower() == 'n':
            print("\nOkay, Have a nice day mate!\n")
calc_main_one()

print("Thank you for using this calculator!\nHave a nice day bro")
