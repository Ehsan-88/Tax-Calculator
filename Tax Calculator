from colorama import init, Fore, Style, Back

init(autoreset=True)

MYCOLOR = '\033[38;2;173;216;230m'    #Custom Color
RESET = Style.RESET_ALL

e = "--------------------------------------"

print(" ")
print(Back.LIGHTBLUE_EX + Style.BRIGHT + "Welcome To Tax Calculator V.1.0")
print(Style.BRIGHT + "© 2024 Ehsan AlaviNahad | Python V.3.13.0")
print(" ")
print(Fore.LIGHTBLUE_EX + "Tax Rate for Toman in 1403:")
print(e)
print("From 0          to 12,000,000 = 0%")
print("From 12,000,000 to 20,000,000 = 15%")
print("From 20,000,000 to more       = 20%")
print(e)

while True:
    income = input("Enter your monthly income: ")
    income = income.replace(",", "")

    if not income.isdigit():
        print("Invalid input. Please enter a valid number.")
        continue

    income = int(income)
    
    tax = 0
    
    if income <= 12000000:
        tax = 0

    elif income <= 20000000:
        tax = (income - 12000000) * 15 // 100

    else:
        # Calculate tax for the portion between 12,000,000 and 20,000,000
        tax += (20000000 - 12000000) * 15 // 100
        tax += (income - 20000000) * 20 // 100
    final_result = income - tax

    percentage = (tax / income) * 100 if tax > 0 else 0

    if tax == 0:
        print(e)
        print(Fore.RED + f"Tax Rate: {percentage:.2f}%")
        print(Fore.YELLOW + f"Tax Payment: ${tax:,}")
        print(Fore.LIGHTGREEN_EX + f"Final Result: ${income:,}")
        print(e)
        print(MYCOLOR + "Looks like you’ve dodged the tax bracket! Must be nice to keep more of your hard-earned cash!")
    else:
        print(e)
        print(Fore.RED + f"Tax Rate: {percentage:.2f}%")
        print(Fore.YELLOW + f"Tax Payment: ${tax:,}")
        print(Fore.LIGHTGREEN_EX + f"Final Result: ${final_result:,}")
        print(e)
        print(MYCOLOR + "Looks like you’ve hit the tax bracket! Guess you’ll be funding the government’s coffee budget!")

    repeat = input("Do you want to try again? (Y/N): ").strip().lower()
    if repeat != "y":
        break
