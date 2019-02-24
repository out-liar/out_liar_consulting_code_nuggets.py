# out_liar_consulting_code_nuggets
A ongoing library of sections of code (mainly functions) that will be useful for future projects.
Prioritised on the basis of how useful the code is for data analysis.

--------------------------------------------------------------------------------------------------------------------------------
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
# Purpose: 
# Use:








--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:





--------------------------------------------------------------------------------------------------------------------------------
# Purpose: 
# Use:





