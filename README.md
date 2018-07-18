# survivor_game
"""
version 3,survivor game
"""
from collections import deque
def survivor(total):
    qlst_survivor1 = deque(list(range(1, total + 1)))
    while len(qlst_survivor1) != 1:  #剩余元素数大于1，继续下一轮 
        qlst_survivor1.remove(qlst_survivor1[1]) #第二个元素毙掉，后面元素往前顺位+1
        qlst_survivor1.rotate(-1)  #所有元素顺位再往前+1
    else:
        print('the survivor is {}'.format(qlst_survivor1[0]))
        
if __name__ == "__main__":
    total = int(input('Please enter the total number of people enrolling the game:[11] '))
    survivor(total)
