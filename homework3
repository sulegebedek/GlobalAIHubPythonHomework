import random
name = input("Enter your name: ")
print("\n******--> Welcome "+name+":) Let's start. <--******\n\n--The word you're going to guess is an animal.\n--If you want to quit the game, press the '*' key.")


image = [  """
                   --------
                   |      |
                   |      O
                   |     \\|/
                   |      |
                   |     / \\
                   -
                   """,
                   """
                   --------
                   |      |
                   |      O
                   |     \\|/
                   |      |
                   |     /
                   -
                   """,
                   """
                   --------
                   |      |
                   |      O
                   |     \\|/
                   |      |
                   |
                   -
                   """,
                   """
                   --------
                   |      |
                   |      O
                   |     \\|
                   |      |
                   |
                   -
                   """,
                   """
                   --------
                   |      |
                   |      O
                   |      |
                   |      |
                   |
                   -
                   """,
                   """
                   --------
                   |      |
                   |      O
                   |
                   |
                   |
                   -
                   """
    ]

words = ["elephant","bird","dolphin","ciraffe"]
word = random.choice(words) 
predict = 5
letters = []

x = len(word)
z = list('_' * x)

print( """
          --------
           |     | 
           |
           |      
           |
           |
           |
           -\n""")
print(' '.join(z), end='\n\n')

while predict >= 0:
    y = input("\nGuess a letter : ")
    if y == '*':
      print("\nGame over because you left the game.")
      break

    elif y in letters:
        print("\nPlease do not guess the letters you guessed before ...")
        continue
    
    elif len(y) > 1:
        print("\nPlease guess only one letter!")
        continue

    elif y not in word:   
      
        print(image[predict])
        predict -= 1
        print(' '.join(z), end='\n')
        print("\nWrong guess! :(  You have {} guess left..".format(predict+1))

    else:
        for i in range(len(word)):
            if y == word[i]:
              z[i] = y
              letters.append(y)
              print("\nRight guess :)")           
        print(' '.join(z), end='\n')
    letters.append(y)

    question = input("\nDo you want to guess the whole word? (y/n) : ")

    if question == "y":
        answer = input("\nEnter your word prediction : ")
        if answer == word:
            print("\nCongratulations you won :))")
            break
        else:
            predict -= 1
            print("\nWrong guess! :(  You have {} guess left..".format(predict+1))


    if predict == -1:
        print("\nYour right to predict is over, try again. You lost! :( ")
        break

