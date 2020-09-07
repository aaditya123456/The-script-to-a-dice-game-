# The-script-to-a-dice-game-
This dice game will be made with Python, so be sure to have a Python app and enviorment!

import random

def main():
    player1 = 0
    player1wins = 0
    player2 = 0
    player2wins = 0
    rounds = 1

    while rounds  != 10:
        print("Round " + str(rounds))
        player1 = dice_roll()
        player2 = dice_roll()
        print("Player 1 roll: " + str(player1))
        print("Player 1 roll: " + str(player2))

        if player1 == player2:
            print("draw!\n")
        elif player1 > player2:
            player1wins = player1wins + 1
            print("Player 1 wins!\n")
        else:
            player2wins = player2wins + 1
            print("Player 2 wins!\n")

        rounds = rounds + 1
    if player1wins == player2wins:
        print ("Draw!")
    elif player1wins > player2wins:
        print("Player 1 wins - Rounds Won: " + str(player1wins))
    else:
        print("Player 2 wins - Rounds Won: " + str(player2wins))
def dice_roll():
    diceRoll = random.randint(1, 6)
    return diceRoll

main()
