def addd(x,y):
    print("\nAddition=",x+y,"\n")

def sub(x,y):
    print("\nSubstraction=",x-y,"\n")

def mul(x,y):
    print("\nMultiplication=",x*y,"\n")

def div(x,y):
    print("\nDivision=",x/y,"\n")

def main():
    while True:
        print(" 1.addition\n 2.substraction\n 3.Multiplication\n 4.division\n")
        ch=int(input("\nenter the choice: "))
        
        if ch==1:
            a=int(input("\nEnter the first number: "))
            b=int(input("\nEnter the second number: "))
            addd(a,b)
        elif ch==2:
            a=int(input("\nEnter the first number: "))
            b=int(input("\nEnter the second number: "))
            sub(a,b)
        elif ch==3:
            a=int(input("\nEnter the first number: "))
            b=int(input("\nEnter the second number: "))
            mul(a,b)
        elif ch==4:
            a=int(input("\nEnter the divident: "))
            b=int(input("\nEnter the divisor: "))
            div(a,b)
        else:
            print("\nWrong input\n4")

    
main()       
