'''
Created on Feb 16, 2017

@author: Audrey
'''
from random import randint 
 
def guess_game():
    random_number = randint(1,100)
    print "Welcome to Guess my number! \nTry guessing the number I am thinking of between 1 and 100 "
    print "You can stop the game any time by typing 'STOP'"
    guesses_count = 0
    points = 150
    free_guesses = 3
    play = True
   
    
    while play:
        guess = raw_input ("Enter your guess: ")
        
        if guess == 'STOP':
            print "Game over, my number was %s" %(random_number)
            break
            
        try:
            guess = int(guess)
        except ValueError:
            print "You must enter a number!"
            continue
        
        if guess > 100 or guess < 1:
            print "Oops you must choose a number between 1 and 100"
            continue
        
        guesses_count += 1
        free_guesses -= 1
        
        if points < 10:
            print "Game Over! You don't have enough points left! My number was %d" %(random_number)
            play = False
            
        if guesses_count == 3 and guess != random_number :
            if guess > random_number:
                print "Sorry %s is too high" %(guess)
                points -= 10
            elif guess < random_number:
                print "Sorry %d is too low" %(guess)
                points -= 10   
            hint = raw_input("You have finished your free guesses, guess now cost 5 points \n do you want a hint for 5 points? enter Y or N: ")
            while hint != 'Y' and hint != 'N':
                hint = raw_input("Please print 'Y' or 'N' only:  ")   
            if  hint == 'Y'   or hint == 'y':
                points -= 5
                if random_number % 2 == 0:
                    print "it is an even number"
                else:
                    print "it is an odd number"
                continue   
            else:
                continue
                
                
        if guesses_count == 6 and guess != random_number :
            if guess > random_number:
                print "Sorry %s is too high" %(guess)
                points -= 10
            if guess < random_number:
                print "Sorry %s is too low" %(guess)
                points -= 10
            hint = raw_input("You have %s left do you want a hint for 10 points? enter Y or N :" %(points))
            while hint != 'Y' and hint != 'N':
                hint = raw_input("Please print 'Y' or 'N' only:  ")      
            if  hint == 'Y':
                points -= 10
                if random_number % 3 == 0:
                    print "it is an multiple of 3"
                elif random_number %4 == 0:
                    print "it is a multiple of 4"
                elif random_number % 5 == 0:
                    print "It is a multiple of 5"
                else:
                    print "It is a not divisible by 3, 4 or 5"
                continue  
            else:
                continue

                
        if guesses_count == 9 and guess != random_number:
            if guess > random_number:
                print "Sorry %s is too high" %(guess)
                points -= 10
            if guess < random_number:
                print "Sorry %s is too low" %(guess)
                points -= 10
            hint = raw_input("You have %s points left do you want a hint for 15 points? enter Y or N :" %(points))   
            while hint != 'Y' and hint != 'N':
                hint = raw_input("Please print 'Y' or 'N' only:  ")   
            if  hint == 'Y'   or hint == 'y':
                points -= 15
                if random_number > 93:
                    print "my number is greater than 93"
                elif random_number < 7:
                    print "My number is less than 7"
                else:
                    print "my number is between %s and %s" %(random_number-(randint(0,3)),random_number+(randint (4,7)))
                continue
            else:
                continue
                         
                 
                  
        if guess > random_number and points >= 10:
            if free_guesses > 0:
                print "%s is too high! Try again you have %s free_guesses guess" %(guess,free_guesses)
            else:
                print "%s is too high! Try again, you have %s points:" %(guess,points)
                points -= 10
                
        if guess < random_number and points >= 10:
            if free_guesses > 0:
                print "%s is too low! Try again you have %s free_guesses guess" %(guess,free_guesses)
            else:
                print "%s is too low! Try again, you have %s points: " %(guess,points)
                points -= 10
            
        if guess == random_number :
            print "You win! you guessed my number %s in %s attempts" %(random_number,guesses_count)
            print "You scored  %s points out of 150" %(points)
            play = False

                   
    else:
        replay = raw_input("Do you want to play again? Type 'Y' or 'N' ")
        while replay != 'Y' and replay != 'N':
            replay = raw_input("Please print 'Y' or 'N' only:  ")
        if replay == 'Y':
            guess_game()
        elif replay == 'N' :  
            print "Thank you for playing!"
                    
                  


guess_game()





