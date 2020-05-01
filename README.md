# Stone-Paper-scissors
print("== WELCOME TO ROCK PAPER SCISSORS GAME ==")

comp1=0

user1=0

while True:
    import random
    list=["rock","paper","scissors"]
    comp=random.choice(list)

    user=input("\nEnter your choose rock/paper/scissors: ")
    if(comp=="rock" and user=="scissors" or
        comp=="paper" and user=="rock" or
        comp=="scissors" and user=="paper"):
        print("computer chose=",comp)
        print("====computer wins!====")
        comp1+=1
        print("Computer count=",comp1)

    elif(user=="rock" and comp=="scissors" or
        user=="paper" and comp=="rock" or
        user=="scissors" and comp=="paper"):
        print("computer chose",comp)
        print("====user wins!==== ")
        user1+=1
        print("User count=",user1)

    elif(user==comp):
        print("\n====Match Tie====\n Enter again")

    else:
        print("\nEnter valid name")

    if(comp1==5 or user1==5):
        print("\n============== GAME OVER ===============")
        print(f"computer wins={comp1} times")
        print(f"User wins={user1} times")

        userint=input("\nDo You want to continue yes/no: ")
        if(userint=='yes'):
            comp1=0
            user1=0
            continue
        else:
            print("\n======== Thank You For Your  Participaption ===============")
            break


