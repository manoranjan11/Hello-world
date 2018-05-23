from random import randint
# for random function

print('{:^100}'.format("EPIC SHOWDOWN:FIGHT THANOS"))


avengers = ["1.Iron man", "2.Captain america", "3.Thor", "4.Dr.Strange", "5.Iron Spider", "6.Black Widow",
            "7.Scarlet Witch", "8.Hawk Eye", "9.Hulk", "10.Vision", "11.The war machine", "12.Black panther",
            "13.Ant Man", "14.Drax", "15.Mantis", "16.Gamora", "17.Groot", "18.Rocket", "19.Winter Soldier", "20.Loki",
            "21.Falcon", "22.Star Lord", "23.Wasp", "24.Captain Marvel", "25.Nebula"]
# storing the list of avengers

print('\n\n')
for avenger in avengers:
    print("%s \n" % avenger)
# printing them

rate_avengers = {"1.Iron man": 24, "2.Captain america": 20, "3.Thor": 25, "4.Dr.Strange": 25, "5.Iron Spider": 22,
                 "6.Black Widow": 18, "7.Scarlet Witch": 23, "8.Hawk Eye": 18, "9.Hulk": 22, "10.Vision": 20,
                 "11.The war machine": 19, "12.Black panther": 23, "13.Ant Man": 23, "14.Drax": 15, "15.Mantis": 15,
                 "16.Gamora": 17, "17.Groot": 21, "18.Rocket": 15, "19.Winter Soldier": 15, "20.Loki": 20,
                 "21.Falcon": 18, "22.Star Lord": 10, "23.Wasp": 21, "24.Captain Marvel": 25, "25.Nebula": 15}
# points for each avenger out of 25

avenger1 = randint(1, 25)
temp = randint(1, 25)
while temp == avenger1:
    temp = randint(1, 25)
avenger2 = temp
# to check both the random integers are different


print('\nYou have 2 members in your team:')

if avenger1 > 9:
    for i in range(3, len(avengers[avenger1-1])):
        print("%s" % avengers[avenger1-1][i])
    print("\nand\n")
else:
    for i in range(2, len(avengers[avenger1-1])):
        print("%s" % avengers[avenger1-1][i])
    print("\nand\n")

if avenger2 > 9:
    for i in range(3, len(avengers[avenger2-1])):
        print("%s" % avengers[avenger2-1][i])
else:
    for i in range(2, len(avengers[avenger2-1])):
        print("%s" % avengers[avenger2-1][i])
# printing them

print('\n')
avenger3 = 0
while avenger3 == 0:
        avenger3 = int(input("Choose your 3rd avenger:"))
        if avenger3 == avenger2 or avenger3 == avenger1:
            print("The member is already in your team")
            avenger3=0
        else:
            break
avenger4 = 0
while avenger4 == 0:
        avenger4 = int(input("Choose your 4th avenger:"))
        if avenger4 == avenger2 or avenger4 == avenger1:
            print("The member is already in your team")
            avenger4 = 0
        else:
            break
# to ensure user doesnt choose already choosed avenger

score = rate_avengers['%s' % avengers[avenger1 - 1]] + rate_avengers['%s' % avengers[avenger2-1]] + rate_avengers['%s' % avengers[avenger3-1]] + rate_avengers['%s' % avengers[avenger4-1]]

print('\nYour possibility for defeating thanos(out of 100 points):\n')
print(score)
# showing the score
if avenger1 == 22 or avenger2 == 22 or avenger3 == 22 or avenger3 == 22:
    print("So sad that your team has star lord.Thanos escpaes")
# sarcasm
