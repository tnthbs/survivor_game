# survivor_game
def survivor(total):
    lst_survivor1 = list(range(1, total + 1))
    print(lst_survivor1)

    while len(lst_survivor1) != 0:  #剩余元素大于1，继续下一轮
        if len(lst_survivor1) == 1:
            print(lst_survivor1)
            break
        
        elif len(lst_survivor1) % 2 == 0: #如果存活人数为偶数，第 0，2，4*存活
            lst_survivor1 = lst_survivor1[0::2]
            print(lst_survivor1)
            if len(lst_survivor1) == 1: #如果切完只剩一个元素时，停止循环
                break
            
        else:
            lst_survivor1 = lst_survivor1[2::2] #如果存活人数为奇数，第 2，4，6*存活，第0位元素被最后一位淘汰
            print(lst_survivor1)
            if len(lst_survivor1) == 1: #切完只剩一个元素时，停止循环，如 1，2，3 > 切完剩下3，停止循环
                break
            
if __name__ == "__main__":
    total = int(input('Please enter the total number of people enrolling the game:[11] '))
    survivor(total)
