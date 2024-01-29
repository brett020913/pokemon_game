name = input('Hello, what is your name? ')
score = 0
attempts = 0

# while loop to allow multiple attempts and first question #
while attempts < 3:
    play_game = input('Hi, '+name+' do you want to play a game? ')

    if attempts < 2 and play_game.lower() == 'yes':
        number_1 = input('Good, your first question is, how many pokemon are there in the first generation? A.134 b.150 C.200 D.100 ' )
        break

    elif attempts < 2 and play_game.lower() == 'no':
        print('Goodbye ' +name+ '!')
        quit()
        break

    elif attempts == 2 and play_game.lower() == 'yes':
        number_1 = input('Finally, your first question is, how many pokemon are there in the first generation? A.134 b.150 C.200 D.100 ')
        break

    elif attempts == 2 and play_game.lower() == 'no':
        print('finally, goodbye!')
        quit()
        break

    else:
        print('Your answer needs to be yes or no! Please answer now. ')
        attempts += 1


if attempts == 3:
    print('You need to read the instructions! Goodbye!')
    quit()


# answer check for question 1 #
if number_1.lower() == 'b' or number_1 == 150 or number_1.lower() == 'b.150':
    print('Correct!')
    score += 1
else:
    print('incorrect!')



# question 2 and answer check for question 2 #
number_2 = input('Your next question is, what is Hitmonlees typing? A.fire B.water C.fighting D.ghost ')

if number_2.lower() == 'c' or number_2.lower() == 'c.fighting' or number_2.lower() == 'fighting':
    print('Correct!')
    score += 1
else:
    print('No thats not right!')

# question 3 and answer check for question 3 #
number_3 = input(name+ ' your next question is, what does Growlithe evolve into? A.Arcanine B.Ninetails C.Vulpix D.Charizard ')

if number_3.lower() == 'a' or number_3.lower() == 'a.arcanine' or number_3.lower() == 'arcanine':
    print('Your on a roll!')
    score += 1
else:
    print('Thats wrong!')

# question 4 and answer check for question 4 #
number_4 = input('One more question after this one, what pokemon is number 1 in the pokedex? A.Pikachu B.Bulbasaur C.Snorlax D.Rhydon ')

if number_4.lower() == 'b' or number_4.lower() == 'b.bulbasaur' or number_4.lower() == 'bulbasaur':
    print('Correct!')
    score += 1
else:
    print(name+' your wrong!')

# question 5 and answer check for question 5 #
number_5 = input('This is the last question, Tyranitar is from generation 1, TRUE OR FALSE? A.True B.False ')

if number_5.lower() == 'b' or number_5.lower() == 'b.false' or number_5.lower() == 'false':
    print('Correct!')
    score += 1
else:
    print(name+' that is incorrect!')

# display scoring #
if score == 0:
    print('You need to study, you didnt get any questions right!')
elif score <= 2:
    print('Better luck next time, you only got ' + str(score) + ' out of 5 right! Hope you had fun!')
elif score <= 4:
    print('Thanks for playing, you got ' + str(score) + ' out of 5 right! Hope you had fun!')
else:
    print('Your a pokemon master! You got ' + str(score) + ' out of 5 right!')

print(str((score/5)*100) + '%')
