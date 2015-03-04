# gamblers-ruin
#statistics simulation

from random import randint
profit = 0
money=1
turn=1
n=100000

while turn <n+1:
    print "turn", + turn
    money=1
    while money>0 and money <11:
        flip = randint(0,1)
        print "flips is",flip
        if flip == 0:
            money = money-1
        else:
            money = money + 1
    if money == 0:
        print "lost a dollar"
        profit = profit -1
    else :
        print "won 10 bucks"
        profit = profit + 10 
    turn=turn+1
profit= float(profit)
average_profit= profit/n
print "average winning is", average_profit
