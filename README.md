# Bomb-defusal-game-Version-1
A simple question and answer game
# counters
correct = 0
chances = 2
# Intro
print('Defuse the bomb!')
#Questions
#1
print('Which wires do you cut? ')
w = input('1.Red   2.Blue   3.Green: ')
ans = '3'
if w == ans:
    print('Well done, on to the next! ')
    correct += 1
else:
    print('It didnt work')
    chances -= 1
print()
#2
b = input('Do you turn off the battery before the fuse? (Y/N): ')
ans= 'y'
if b.lower()== ans:
    print('Good, one more remaining.')
    correct += 1
else:
    print('wrong!')
    chances -= 1
if chances == 0:
    print('Used up all the chances. BOOM!!!!')
    exit()
print()
#3
print('Still trying to save yourself from being blown, solve this equation.')
m = input('11 - 2 = 3x: ')
if m.isdigit():
    m = int(m)
else:
    print('Not a number')
ans = 3
if m == ans:
    print('Correct!')
    correct += 1
else:
   chances -= 1
   print('WRONG!!!')
if chances == 0:
    print('Used up all the chances. BOOM!!!!')
    exit()
print()
#message 
print(f'You got {correct} out of 3 questions correct.')
print('Bomb Defused, you lived to see another day.')
