from tkinter import *
import random

def next_turn(row, column):

    global player

    if buttons[row][column]['text'] == "" and check_winner() is False:

        if player == players[0]:

            buttons[row][column]['text'] = player

            if check_winner() is False:
                player = players[1]
                label.config(text=(players[1] + " turn"))

            elif check_winner() is True:
                label.config(text=(players[0] + " wins"))

            elif check_winner() == "Tie":
                label.config(text=("Tie!"))

        else:

            buttons[row][column]['text'] = player

            if check_winner() is False:
                player = players[0]
                label.config(text=(players[0] + " turn"))

            elif check_winner() is True:
                label.config(text=(players[1] + " wins"))

            elif check_winner() == "Tie":
                label.config(text=("Tie!"))

def check_winner():

    row: int
    for row in range(3):
        if buttons[row][0]['text'] == buttons[row][1]['text'] == buttons[row][2]['text'] != "":
            buttons[row][0].config(bg="Orange")
            buttons[row][1].config(bg="Orange")
            buttons[row][2].config(bg="Orange")
            return True

    for column in range(3):
        if buttons[0][column]['text'] == buttons[1][column]['text'] == buttons[2][column]['text'] != "":
            buttons[0][column].config(bg="Orange")
            buttons[1][column].config(bg="Orange")
            buttons[2][column].config(bg="Orange")
            return True

    if buttons[0][0]['text'] == buttons[1][1]['text'] == buttons[2][2]['text'] != "":
        buttons[0][0].config(bg="Orange")
        buttons[1][1].config(bg="Orange")
        buttons[2][2].config(bg="Orange")
        return True

    elif buttons[0][2]['text'] == buttons[1][1]['text'] == buttons[2][0]['text'] != "":
        buttons[0][2].config(bg="Orange")
        buttons[1][1].config(bg="Orange")
        buttons[2][0].config(bg="Orange")
        return True

    elif empty_spaces() is False:

        for row in range(3):
            for column in range(3):
                buttons[row][column].config(bg="Yellow")
        return "Tie"

    else:
        return False

def empty_spaces():

    spaces = 9

    for row in range(3):
       for column in range(3):
           if buttons[row][column]['text'] != "":
             spaces -=1

    if spaces == 0:
       return False
    else:
       return True

def new_game():

    global player

    player = random.choice(players)

    label.config(text=player+" turn")

    for row in range(3):
        for column in range(3):
            buttons[row][column].config(text="",bg="#F0F0F0")

window = Tk()
window.title("Tic-Tac-Toe")
players = ["x","o"]
player = random.choice(players)
buttons = [[0,0,0],
           [0,0,0],
           [0,0,0]]

label = Label(text=player + " turn", font=("Ink Free",40))
label.pack(side="top")

reset_button = Button(text="restart", font=("Ink Free",20), command=new_game)
reset_button.pack(side="top")

frame = Frame(window)
frame.pack()

for row in range(3):
    for column in range(3):
        buttons[row][column] = Button(frame, text="",font=("Ink Free",40), width=5, height=2,
                                       command=lambda row=row, column=column: next_turn(row, column))
        buttons[row][column].grid(row=row,column=column)

window.mainloop()


def heroic_courage2():
    print_delayed("You pull the sheet away and out came....")
    print_delayed("THE GHOST itself,all your friends shriek and hide behind you!")
    print_delayed("Now you got no other option but to face it!!")
    print_delayed("You pull out your bottle of gas and are about to open the lid when,")
    print_delayed("the ghost throws a piece of wood at you,your are forced to dodge,")
    print_delayed("resulting in dropping the bottle.")
    choices_7()

def heroic_courage3():
    print_delayed("You throw the wood back at it,now its furious and comes at you,")
    print_delayed("You whisper to your friend and run off between the covered things.")
    print_delayed("The ghost follows you around the attic while throwing things at you!")
    print_delayed("You are about to reach your friends when you give the signal to your friend.")
    print_delayed("He throws the bottle towards you & at the last sec you jump to your left,")
    print_delayed("cuz you were in front of the ghost till the last sec,it didn't see the bottle & got hit.")
    print_delayed("Now the ghost is very angry & charges at your friend!")
    print_delayed("You quickly get up & light your gas lighter & throw it at the ghost.")
    print_delayed("The fire quickly envelops the ghost as it screams in agony,")
    print_delayed("it stumbles on the furniture's as the fire spreads in the attic!!")
    print_pause("[You & your friends jump out from the burned roof and escape,")
    print_pause("the house is burning behind you as you do a high5 with 'that' friend and run off!]")
    print_pause("{Congratulation!!You escaped the haunted house!}")
    play_again()


def last_struggle():
    print_delayed("You try to find the fireplace and light it with your last matches.")
    print_delayed("As soon as you light it, you guys see the whole house bricked up!!")
    print_delayed("Its as if the house itself is trying to trap you guys in there!!")
    print_delayed("Suddenly the ghost shows its self,it has long sharp nails,")
    print_delayed("its clothes stained with blood,it stares at you all with its scary face..")
    print_delayed("it suddenly disappears,you look to your right where your friend was...")
    print_delayed("as he fall's,your eyes widen with horror as your all friends are taken down!")
    print_delayed("Now its your turn,as you fall and crawl back in fear,it jumps on you....")
    print_delayed("The End")
    print_delayed("You died :(")
    play_again()

def last_struggle2():
    print_delayed("You run to pick up the bottle and when you reach the bottle,")
    print_delayed("You hear your friend scream!You turn around to see the ghost charging at them!!")
    print_delayed("Its too late for you to return cuz the ghost is fast as lightning..")
    print_delayed("You take the bottle and run towards the ghost to hit it with accuracy,")
    print_delayed("but you failed to hit it as it finishes you off in a flash!")
    print_pause("You Died =[ ")
    print_pause("Game Over!!")
    play_again()
def story_names2():
    print_pause("Do you want to play the other story or play this again?: (yes/no)")
    while True:
        choice = input("Pls enter 'yes' to play new game,'no' to play again: ")
        if choice == "yes":
            print_delayed("Excellent! Starting the 2nd game...")
            play_2nd()
            break
        elif choice == "no":
            print_delayed("Thanks for playing!.")
            play_again()
            break
        else:
            print_pause("Sorry, Please enter yes or no: ")

def play_again():
    print_pause("Would you like to play again?")
    print_pause("Pls enter (yes/no): ")
    while True:
        response = input().lower()
        if response == "yes":
            print_pause("{Excellent! Restarting the game ...}")
            intro_story2()
        elif response == "no":
            print_pause("Sorry, Please enter yes or no: ")
        else:
            print_pause("Thanks for playing!Hope you enjoyed!")
            break

def play_game():
    name
    items.clear()
    story_names()
    intro_story1()
    intro_story2()
    choose_path_story1()
    choose_path_story2()

def play_2nd():
    intro_story2()
    choose_path_story2()

items = []
play_game()

