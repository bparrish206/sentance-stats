sentance-stats
==============

#main function 
def main():
# ask user for sentence to run
    sentence = input('Enter a sentence: (return to exit)')
    #Validate input and run sequence
    while len(sentence) >= 1:
        printStats(sentence)
        #Give use option to repeat or end program
        sentence = input('Enter a sentence: (return to exit)')

# calculates the users's input
def printStats(input):
    print('Statistics on your sentence: ')
    print('   Characters:', charCount(input))
    print('   Letters:', letterCount(input))
    print('   Upper-case:', upperCase(input))
    print('   Lower-case:', lowerCase(input))
    print('   Digits:', digitCount(input))
    print('   Spaces:', spaceCount(input))
    print('   Word characters:', wordCharacters(input))
    print('   Punctuation:',  punctuation(input))
    
#counts the length of the sentence
def charCount(sentence):
    return len(sentence)

# counts the number of letters in sentence
def letterCount(sentence):
        total = 0
        #basic loop tests to see if charecter is a letter if so adds 1 to total.
        for lt in sentence:
            if lt.isalpha() == True:
                total += 1
        # returns total results
        return total
# Counts all upper case letters in sentence
def upperCase(sentence):
    total = 0
    #loop tests each charecter if uppercase adds count of one.
    for uc in sentence:
        if uc.isupper() == True:
            total +=1
    #returns total
    return total

# Counts all lower case charecters
def lowerCase(sentence):
    total = 0
    #tests each charecter if lower case adds one
    for lc in sentence:
        if lc.islower() == True:
            total +=1
    #returns total
    return total

#counts number of digits
def digitCount(sentence):
    total = 0
    #checks each charecter if digit adds one
    for dg in sentence:
            if dg.isdigit() == True:
                total += 1
    #returns total
    return total

#counts spaces
def spaceCount(sentence):
    total = 0
    #check each charecter is blank space adds one
    for sp in sentence:
        if sp.isspace() == True:
            total += 1
    #returns one
    return total

#counts word charecters
def wordCharacters(sentence):
    total = 0
    #checks each charecter if a word charecter adds one to total
    for  wc in sentence:
        if wc in ['$',  '#', '@', '%', '&', '+', '-', '=', '<', '>', '*', '/']:
            total += 1
    #returns total
    return total

#counts punctuation
def punctuation(sentence):
    total = 0
    #loops through the sentence and if punction mark adds one to total
    for pct in sentence:
        if pct in ['!', '~', '`', '^', '(', ')', '_', '{', '}', '[', ']','|', '\'', ';', ':','"',"'", ',', '.', '?']:
            total += 1
    #returns total
    return total

#calls main
main()
