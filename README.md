# Coding-projects
## To make a Number Game    
    import random  
    x=int(input("Enter Number to play : "))
    for i in range(24):
        randomnumber=random.randint(2,9)
        print(f"{x} x {randomnumber} = ",end="")
        andswer=int(input("Enter your answer : "))
        if andswer==x*randomnumber:
            print("✔")
        else:
            print(f"\n Wrong Answer. Correct answer is  {x*randomnumber}")  

## Sample run  

    Enter Number to play : 12  
    12 x 2 = Enter your answer : 24  ✔  
    12 x 8 = Enter your answer : 545  
    
    Wrong Answer. Correct answer is 96  
    12 x 3 = Enter your answer :    
