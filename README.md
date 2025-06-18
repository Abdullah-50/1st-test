# Story game
import time

name = input("Hello what is your name?: ")
print("Welcome to story_teller " + name)

def print_pause(message, delay=1):
    print(message)
    time.sleep(delay)

def print_delayed(message, delay=0.04):
    for char in message:
        print(char, end='', flush=True)
        time.sleep(delay)
    print()

def story_names():
    print_pause("Which story game would you like to play?")
    print_pause("1.The goblin king.")
    print_pause("2.The Haunted House")
    while True:
        choice = input("Please select 1 or 2: ")
        if choice == '1':
            intro_story1()
        elif choice == '2':
            intro_story2()
        else:
            print("Sorry pls enter 1 or 2: ")

def intro_story1():
    print_delayed("Ok,lets get started.So the story begins as...")
    print_delayed("You find yourself standing in an open field, filled with grass and black thorny roses.")
    print_delayed("Rumors say that a wicked ogre (Goblin King) is somewhere around here,")
    print_delayed("and has been terrifying the nearby village.")
    print_delayed("In front of you is a house.")
    print_delayed("To your right is a dark cave.")
    print_delayed("In your hand you have a rusty dagger.")
    print_delayed("You have 2 choices:")
    choose_path_story1()

def intro_story2():
    print_delayed("Okay,lets get started.So the story begins....")
    print_delayed("As rain pelted the window panes, you sat in the living room of the old Barker House.")
    print_delayed("A place rumored to be haunted by its former inhabitants.")
    print_delayed("You and your friends had dared each other to spend the night.")
    print_delayed("But as midnight approached, the wind’s howling seemed to carry voices.")
    print_delayed("Suddenly, the lights flickered and went out.")
    print_delayed("The only light now came from the fireplace, casting eerie shadows across the room.")
    print_delayed("You have 2 choices:")
    choose_path_story2()

def choose_path_story1():
    print_pause("1. {Knock on the door of the house.}")
    print_pause("2. {Peer into the cave.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            house()
            break
        elif choice == '2':
            cave()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")

def house():
    print_delayed("You approach the door of the house.")
    print_delayed("You are about to knock when the door opens and out steps a goblin.")
    print_delayed("Uh oh! It's the goblin's house!")
    print_delayed("The goblin attacks you!")
    if "sword" in items:
        fight()
    else:
        print_delayed("You feel a bit unprepared for this,what with only having a tiny dagger.")
        print_delayed("The goblin jumps and slashes you,")
        print_delayed("and everything becomes dark...")
        print_pause("Game over!")
        play_again()
def cave():
    print_delayed("You peer cautiously into the cave.")
    if "sword" in items:
        print_delayed("You've been here before, and gotten all the good stuff. It's just an empty cave now.")
    else:
        print_delayed("It turns out to be only a very small cave.")
        print_delayed("Your eye catches a glint of metal behind a rock.")
        print_delayed("You have found the legendary Sword 'Dark Blade'!")
        print_delayed("You discard your silly old dagger and take the sword with you.")
        items.append("sword")
        print_delayed("You walk back out to the field.")
    choose_path_story1()

def fight():
    print_delayed("As the goblin moves to attack,you unsheath your new sword.")
    print_delayed("The Dark Blade shines brightly in your hand as you brace yourself for the attack.")
    print_delayed("The goblin comes at you and slashes non-stop,you step back while stopping all its attacks.")
    print_delayed("After an hour of intense fight you finish him with the last mighty blow!")
    print_delayed("You sit at the house's entrance and recover your stamina.")
    story_names2()
def choose_path_story2():
    print_pause("1. {Check the fuse box in the basement.}")
    print_pause("2. {Stay by the fire and wait for the lights to come back on their own.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            basement_trip()
            break
        elif choice == '2':
            fixing_fuse()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")

def choices():
    print_pause("1.{Inspect the glowing symbol.}")
    print_pause("2.{Fix the fuse box quickly and return upstairs.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            shadow_glowing_symbol()
            break
        elif choice == '2':
            fuse_box()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")
def choices_2():
    print_pause("1. {Go to the window to investigate the shadow.}")
    print_pause("2. {Ignore it and stay near the safety of the fire.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            shadow_glowing_symbol()
            break
        elif choice == '2':
            fuse_box2()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")

def choices_3():
    print_pause("1. {Touch the symbol.}")
    print_pause("2. {Run back to the safety of the living room.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            symbol()
            break
        elif choice == '2':
            fuse_box2()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")

def choices_4():
    print_pause("1. {Go to the window.}")
    print_pause("2. {Run back to the safety of the living room.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            window()
            break
        elif choice == '2':
            fuse_box2()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")
def choices_5():
    print_pause("1. {Investigate the noises in the attic.}")
    print_pause("2. {Suggest everyone leave the house immediately.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            living_room()
            break
        elif choice == '2':
            print_pause("You decide to leave the house with everyone.")
            print_pause("As you leave, the house seems to sigh with relief.")
            play_again()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")

def choices_5b():
    print_pause("1. {Investigate the noises in the attic.}")
    print_pause("2. {Suggest everyone leave the house immediately.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            living_room()
            break
        elif choice == '2':
            print_pause("You decide to leave the house with everyone.")
            print_pause("As you leave, the house seems to sigh with relief.")
            play_again()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")
def choices_6():
    print_pause("1. {Pull the sheet away.}")
    print_pause("2. {Find a way to relight the fire or escape the house.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            heroic_courage2()
            break
        elif choice == '2':
            last_struggle()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")
def choices_7():
    print_pause("1. {Pull the sheet away.}")
    print_pause("2. {Find a way to relight the fire or escape the house.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            heroic_courage()
            break
        elif choice == '2':
            last_struggle()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")

def choices_8():
    print_pause("1. {Pick up th bottle.}")
    print_pause("2. {Get the ghosts attention.}")
    while True:
        choice = input("Choose 1 or 2: ")
        if choice == '1':
            last_struggle2()
            break
        elif choice == '2':
            heroic_courage3()
            break
        else:
            print_pause("Excuse me? Please choose 1 or 2.")
def basement_trip():
    print_delayed("You grab a flashlight and head to the basement.")
    print_delayed("The stairs creak under your weight, and a cold draft makes you shiver.")
    print_delayed("As you reach the bottom, you see the outline of the fuse box on your left.")
    print_delayed("In front of you is a small window with a strange shadow,")
    print_delayed("and there is a glowing symbol behind the glass.")
    choices()
def fixing_fuse():
    print_delayed("You decide to stay put, hoping the lights would return.")
    print_delayed("But then,one of your friends whispers urgently,'Did you see that shadow move?'")
    print_delayed("Pointing toward the window,you just make out a shadowy figure outside, moving closer.")
    choices_2()
def shadow_glowing_symbol():
    print_delayed("As you approach the shadow,the air turns icy.")
    print_delayed("The figure’s face presses against the glass, its eyes hollow with despair.")
    print_delayed("You feel compelled to do something.")
    choices_3()
def fuse_box():
    print_delayed("You manage to flip the fuses, and the lights flicker back to life.")
    print_delayed("When you return upstairs, you find your friends huddled together,")
    print_delayed("whispering frantically about noises coming from the attic.")
    choices_5b()

def fuse_box2():
    print_delayed("You ignore it and huddle together with your friends,")
    print_delayed("while talking about the noises coming from the attic.")
    choices_5()
def living_room():
    print_delayed("As you & your friends are leaving for the attic,the living room feels colder.")
    print_delayed("As you reach the attic, the door slams shut behind you.")
    print_delayed("In the dim light, you can see old furniture covered in sheets,")
    print_delayed("and one sheet slowly begins to rise.")
    choices_6()


def symbol():
    print_delayed("The moment you touch the symbol,")
    print_delayed("a rush of wind blasts through, extinguishing the fireplace.")
    print_delayed("And u all get teleported to the attic,")
    print_delayed("where every thing is covered with sheets.")
    print_delayed("Suddenly one sheet begins to rise,")
    print_delayed("and u hear a voice saying 'JoIn uS'....")
    choices_6()
def window():
    print_delayed("The moment you open the window,")
    print_delayed("a rush of wind blasts through, extinguishing the fireplace.")
    print_delayed("Darkness envelopes you, and whispers echo around, growing louder, saying, 'Join us'.")
    choices_4()

def heroic_courage():
    print_delayed("You pull the sheet and under it was...")
    print_delayed("The GHOST itself! You panic and fall back.")
    print_delayed("As you are still shocked, your hand touches something behind you.")
    print_delayed("It is a small bottle of gas. Something comes to your mind!")
    print_delayed("You throw the bottle at the ghost as it spills all over its sheet.")
    print_delayed("The ghost laughs and says, 'You can't hurt me with a bottle!,hahaha',but it didn't see the gas spilling.")
    print_delayed("So you quickly throw the last matchstick at the ghost.")
    print_delayed("'WHOOOSHH' a big fire envelopes the ghost as it cries in pain.")
    print_delayed("As the fire is burning brightly, a slight smirk appears on your face ;]")
    print_pause("[You break the door and go down to your friends,as you all are running out of the house..")
    print_pause("the lightning strikes and huge scary shadows are being cast on the ground!!']")
    print_delayed("{Congratulations!!You managed to escape the Haunted House!")
    play_again()


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

