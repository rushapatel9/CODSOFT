import random

small="abcdefghijklmnopqrstuvwxyz"
capital="ABCDEFGHIJKLMNOPQRSTUVWXYZ"
numbers="0123456789"
symbols="!@#$%^&*"

passs=small+capital+numbers+symbols
length=int(input("Enter the length of password: "))

password="".join(random.sample(passs,length))
print("Your Password is: "+password)
