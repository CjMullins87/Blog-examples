Initial_choice_result = []
Switch_choice_result = []

for i in range(1000):

    #Game Setup
    doors = list(range(1,4)) #All possibilities
    win = rand.randint(1,3) #Win condition
    goats = [door for door in doors if door != win] #Lose condition

    #The Game
    first_choice = rand.randint(1,3) #Your selection
    reveal = rand.sample([door for door in goats if door != first_choice], 1) #Host reveal
    switch_choice = [door for door in doors if door != reveal[0] and door != first_choice] #Remaining Choice

    #Result
    if first_choice == win:
        Initial_choice_result.append(1)
        Switch_choice_result.append(0)
    if switch_choice[0] == win:
        Initial_choice_result.append(0)
        Switch_choice_result.append(1)    
        
print('Probability of winning w/ initial choice:', sum(Initial_choice_result)/1000)
print('Probability of winning w/ switch choice:', sum(Switch_choice_result)/1000)
