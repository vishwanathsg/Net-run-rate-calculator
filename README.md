# Net-run-rate-calculator
This code calculates net run rate between 2 teams at a time

#Design and write a program to calculate Net Run Rate scored by the two teams
#To avoid biassed results, the number of over is by default 20, as if a team gets all out before 20 overs, their run rate will not get affected much because the divisor is smaller.
#NOTE: If the difference between the net runrates is very negligiable, it would be considered equal. Then the decision will be made upon the number of overs played.

Run1=float(input("Enter the runs scored by the first team: "))
#User input on first team's runs
"""
Input Run1 should be a positive number
Return True if numerical value entered 
"""

Run2=float(input("Enter the number of runs scored by the opponent team: "))
#User input on second team's runs
"""
Input Run2 should be a positive number
Return True if numerical value entered 
"""

Overs=20
#Predefined overs because all-out team playing less overs will still have a good net runrate

Rate1=Run1//20
Rate2=Run2//20
#Individual runrates of the teams

NRate1=Rate1-Rate2
NRate2=Rate2-Rate1
#Defined net runrate

if NRate1>NRate2: #Compound Statement
    print()
    print("1st team's net runrate is",NRate1) #Suit1
    print("2nd team's net runrate is",NRate2) #Suit2
    print()
    print("The net runrate of the first team is more than that of second team. Thus the first team will top the points table") #Suit3

elif NRate1 == NRate2:
    print()
    print("The net runrate of both the teams are equal. So now we'll have to consider the number of overs played:") #Suit4
    print()
    Over1 = float(input("Enter the number of overs played by the first team: "))
    Over2 = float(input("Enter the number of overs played by the second team: "))

    if Over1<Over2:
        print("Since the first team made the same runs in lesser overs, it will top the position table") #Suit5

    elif Over1 == Over2:
        print()
        print("Since both the teams have played the same number of overs, we'll have to rematch as we don't consider number of wickets left while calculating net runrate") #Suit6

    else:
        print()
        print("Since the second team made the same runs in lesser overs, it will top the position table") #Suit7

else:
    print()
    print("2nd team's net runrate is", NRate2) #Suit8
    print("1st team's net runrate is", NRate1) #Suit9
    print()
    print("The net runrate of the second team is more than that
