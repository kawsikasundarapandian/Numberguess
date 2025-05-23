import random

Easy_level_chances = 6
Hard_level_chances = 4

def set_difficult(level_chosen):
    if level_chosen.lower() == "easy":
        return Easy_level_chances
    else:
        return Hard_level_chances

def check_answer(Num, answer, chances):
    if Num < answer:
        print("Your Guess is low!")
        return chances - 1
    elif Num > answer:
        print("Your Guess is too High!")
        return chances - 1
    else:
        print("Congratulations! Your Guess is correct")
        return chances

def number_guess_game():
    print("Think of a number between 1 to 20")
    answer = random.randint(1, 20)
    print(answer)
    level = input("Choose level of difficulty! Type 'easy' or 'hard': ")
    chances = set_difficult(level)

    if chances != Easy_level_chances and chances != Hard_level_chances:
        print("You have entered an invalid level... play again!")
        return

    Num = 0
    while Num != answer:
        if chances == 0:
            print("Oops! You Lose it")
            return
        print(f"You have {chances} chances remaining to guess the number")
        Num = int(input("Guess a number: "))
        chances = check_answer(Num, answer, chances)
        if Num != answer and chances > 0:
            print("Guess again")

number_guess_game()
