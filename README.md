# out_liar_consulting_code_nuggets.py
A ongoing library of sections of code (mainly functions) that will be useful for future projects.
Prioritised on the basis of how useful the code is for data analysis.

--------------------------------------------------------------------------------------------------------------------------------


                          _,..,,,_
                     '``````^~"-,_`"-,_
       .-~c~-.                    `~:. ^-.
   `~~~-.c    ;                      `:.  `-,     _.-~~^^~:.
         `.   ;      _,--~~~~-._       `:.   ~. .~          `.
          .` ;'   .:`           `:       `:.   `    _.:-,.    `.
        .' .:   :'    _.-~^~-.    `.       `..'   .:      `.    '
       :  .' _:'   .-'        `.    :.     .:   .'`.        :    ;
  jgs  :  `-'   .:'             `.    `^~~^`   .:.  `.      ;    ;
        `-.__,-~                  ~-.        ,' ':    '.__.`    :'
                                     ~--..--'     ':.         .:'
                                                     ':..___.:'

--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Calculate median for a list of numbers.
# Use: Data analysis.

def median(lst):
    sorted_list = sorted(lst)
    if len(sorted_list) % 2 != 0:
        #odd number of elements
        index = len(sorted_list)//2 
        return sorted_list[index]
    elif len(sorted_list) % 2 == 0:
        #even no. of elements
        index_1 = len(sorted_list)/2 - 1
        index_2 = len(sorted_list)/2
        mean = (sorted_list[index_1] + sorted_list[index_2])/2.0
        return mean
       
   
print median([2, 4, 5, 9])

--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Test to identify a number as prime.
# Use: Security.

def is_prime(x):
    if x < 2:
        return False
    else:
        for n in range(2, x-1):
            if x % n == 0:
                return False
        return True
print is_prime(123)


--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Factorioal of a number.
# Use: Probabalistic modelling.

def factorial(x):
    total = 1
    while x>0:
        total *= x
        x-=1
    return total
print factorial(6)


# Purpose: Purify a list of numbers.
# Use: Cleaning data before analysis.

def purify(lst):
    res = []
    for ele in lst:
        if ele % 2 == 0:
            res.append(ele)
    return res
  
print purify([1, 2, 3, 4])

--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Count the number of items in a list.
# Use: For cal culating the median of a list of data.

def count(sequence, item):
    count = 0
    for i in sequence:
        if i == item:
            count += 1
    return count    
print count([1, 2, 1, 1], 1)

--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Censor words in a text.
# Use: Processing data.

def censor(text, word):
    words = text.split()
    result = ''
    stars = '*' * len(word)
    count = 0
    for i in words:
        if i == word:
            words[count] = stars
        count += 1
    result =' '.join(words)

    return result
print censor("O, he gives us what we need, \
It may not be what we want", "we")


--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Remove vowels from a text.
# Use: Processing data.

def anti_vowel(text):
    t=""
    for c in text:
        for i in "ieaouIEAOU":
            if c==i:
                c=""
            else:
                c=c
        t=t+c
    return t
print anti_vowel("Do not go gentle into that good night \
Rage, rage, rage, against the dying of the light.")

--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Reverse letters in a each word, in a string of text.
# Use:

def reverse(text):
    word = ""
    l = len(text) - 1
    while l >= 0:
        word = word + text[l]
        l -= 1
    return word
print reverse("At any given moment, public opinion is a chaos of superstition, misinformation, and prejudice.")



--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Sum digits of a number.
# Use:

def digit_sum(x):
    total = 0
    while x > 0:
        total += x % 10
        x = x // 10
        print x
    return total
print digit_sum(433)

--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Function that takes a number and checks if it is an integer.
# Use: Data processing.

def is_int(x):
    absoluteCount = abs(x)
    typeCount =type(x)
    roundCount = round(absoluteCount)
    if typeCount and absoluteCount - roundCount == 0:
        return True
    else:
        return False
print is_int(7.0)   # True    
print is_int(7.5)   # False    
print is_int(-1)    # True      


--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Checks if an integer is even.
# Use: Data validation.

def is_even(x):
    if x %2 == 0:
        return True
    else:
        return False
        
        
print is_even(900)


--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Calculates the product of numbers in a list.
# Use:

def product(list):
  total = 1
  for num in list:
    total = total * num
  return total

print product([4, 5, 5])


--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Function that removes duplicates in a list.
# Use: Data processing.

def remove_duplicates(inputlist):
    if inputlist == []:
        return []
    
    # Sort the input list from low to high    
    inputlist = sorted(inputlist)
    # Initialize the output list, and give it the first value of the now-sorted input list
    outputlist = [inputlist[0]]

    # Go through the values of the sorted list and append to the output list
    # ...any values that are greater than the last value of the output list
    for i in inputlist:
        if i > outputlist[-1]:
            outputlist.append(i)
        
    return outputlist
  
print remove_duplicates([1, 1, 2, 2])



--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Function that concatenates strings.
# Use:

n = ["Gore", "Vidal"]


def join_strings(words):
    result = ""
    for w in range(len(words)):
        result += words[w]
    return result


print join_strings(n)

--------------------------------------------------------------------------------------------------------------------------------
# Purpose: Take a raw user input and compare it to a value. (Taken from battleship project.)
# Use:

for turn in range(4):
  print "Turn", turn + 1
  guess_row = int(raw_input("Guess Row: "))
  guess_col = int(raw_input("Guess Col: "))

  if guess_row == ship_row and guess_col == ship_col:
    print "Congratulations! You sank my battleship!"  
    break
  else:
    if guess_row not in range(5) or \
      guess_col not in range(5):
      print "Oops, that's not even in the ocean."
    elif board[guess_row][guess_col] == "X":
      print( "You guessed that one already." )
    else:
      print "You missed my battleship!"
      board[guess_row][guess_col] = "X"
    if (turn == 3):
      print "Game Over"
    print_board(board)


--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:



--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:


--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:




--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:



--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:



--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:



--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:








# created for out_liar_consulting




     ,----------------,              ,---------,
        ,-----------------------,          ,"        ,"|
      ,"                      ,"|        ,"        ,"  |
     +-----------------------+  |      ,"        ,"    |
     |  .-----------------.  |  |     +---------+      |
     |  |                 |  |  |     | -==----'|      |
     |  |  I <3 Python    |  |  |     |         |      |
     |  |                 |  |  |/----|`---=    |      |
     |  |                 |  |  |   ,/|==== ooo |      ;
     |  |                 |  |  |  // |(((( [33]|    ,"
     |  `-----------------'  |," .;'| |((((     |  ,"
     +-----------------------+  ;;  | |         |,"     -K.L-
        /_)______________(_/  //'   | +---------+
   ___________________________/___  `,
  /  oooooooooooooooo  .o.  oooo /,   \,"-----------
 / ==ooooooooooooooo==.o.  ooo= //   ,`\--{)B     ,"
/_==__==========__==_ooo__ooo=_/'   /___________,"
`-----------------------------'
