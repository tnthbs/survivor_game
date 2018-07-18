# survivor_game
"""
version 5,survivor game
"""
def survivor(total):
    lst_survivor1 = list(range(1, total + 1))
    while len(lst_survivor1) != 1:  #剩余元素数大于1，继续下一轮  
        if len(lst_survivor1) % 2 == 0: #如果存活人数为偶数，第 1，3，5* 元素死亡
            del lst_survivor1[1::2]           
        else:
            del lst_survivor1[1::2] 
            del lst_survivor1[0]    
    else:                                       #剩余元素为1时打印survivor
       # print('the survivor is {}'.format(lst_survivor1[0]))
            
if __name__ == "__main__":
    total = int(input('Please enter the total number of people enrolling the game:[11] '))
    survivor(total)
