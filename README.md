# survivor_game
"""
version 4,survivor game
"""
def survivor(total):
    i = 1
    while pow(2,i) < total: 
        i += 1
    survivor = 2*(total - pow(2,i-1)) + 1
    print('the survivor is {} '.format(survivor))

if __name__ == "__main__":
    total = int(input('Please enter the total number of people enrolling the game:[11] '))
    survivor(total)
