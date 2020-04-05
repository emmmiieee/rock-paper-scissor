# devil-midget-jesus-game


import random
choice = ["Devil", "Midget", "Jesus"]


user_score = 0
comp_score = 0

while str(user_score < 2) or str(comp_choice < 2):

    print("Your choice of weapon: devil, midget, jesus")
    user_choice = input("Pick your weapon: ")
    comp_choice = random.choice(choice)

    print("You chose: " + user_choice)
    print("Your opponent chose: " + comp_choice)

    if user_choice == "jesus" and comp_choice == "Jesus":
        print("You and your opponent are dead. No winner.")
        user_score = 0
        comp_score = 0
    elif user_choice == "devil" and comp_choice == "Jesus":
        comp_score = comp_score + 1
        print("You are harmed")
    elif user_choice == "devil" and comp_choice == "Midget":
        user_score = user_score + 1
        print("Successful attack")
    elif user_choice == "jesus" and comp_choice == "Midget":
        comp_score = comp_score + 1
        print("You are harmed")
    elif user_choice == "jesus" and comp_choice == "Devil":
        user_score = user_score + 1
        print("Successful attack")
    elif user_choice == "midget" and comp_choice == "Devil":
        comp_score = comp_score + 1
        print("You are harmed")
    elif user_choice == "midget" and comp_choice == "Jesus":
        user_score = user_score + 1
        print("Successful attack")
    else:
        print("Tie, No damage")

    print("Your score: " + str(user_score))
    print("Your opponent's score: " + str(comp_score))

    if user_score == 3:
        print("Victory!!")
        user_score = 0
        comp_score = 0
        print("New Game")
    elif comp_score == 3:
        print("You are DEAD")
        user_score = 0
        comp_score = 0
        print("New Game")
