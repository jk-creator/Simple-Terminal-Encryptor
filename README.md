# Simple-Terminal-Encryptor
This is a short python code to encrypt an 8 char input by displaying the charachters in even indices first followed by those in odd indexes

import time
import sys
import os

# A function to determine the length of the input text
def lenText():
    v = len(validateInput.text)
    print("The length is " +str(v) +" charachters.")


# A function that determines whether the entered data is of the required charachter size
# The assert keyword can also be used to reduce the lines of code
def validateInput(text:str):
    validateInput.text = text
    # print(text) # printing is outputting text to terminal
    lenText()
    v = len(text) # determining the length of text into a var v
    # print(v)
    if v!= 8: # an if else statement 
        
        while v != 8:
            
            text = input("Enter text with 8 charachters:")
            validateInput.text = text
            v = len(text)
            print("Length of text:",v)
            if v ==8:  
                print("Your text is ",text," wait for encryption.") 
            else:
                print("Your text isn\'t 8 chars.")
            if len(text) != 8:
                print("Only 8 charachters allowed, system will exit!")
                time.sleep(10) # stops compilation of code for 10 secs
                os.system('cls') # clears the terminal window
                sys.exit() # closes the terminal window

    else:
        print("Your text is ",text," wait for encryption.")


# A function to decrypt the text input by displaying the charachters in even positions first; then odd last.
def encryptText():
    a = t1[0] # creating a var a and assigning it the first value of t1 lis
    b = t1[1]
    c = t1[2]
    d = t1[3]
    e = t1[4]
    f = t1[5]
    g = t1[6]
    h = t1[7]
    etup = (a,c,e,g,b,d,f,h) # creating a tuple(immutable one dimensional array) with the letters from the text as elements
    print("Your encrypted text is",''.join(etup),".") # '' stores what will separate the tuple charachters and .join() is used to print the tuple as a string.
    pass


# A function to revert encryption
def decryptText():
    a = t1[0] # creating a var a and assigning it the first value of t1 list
    b = t1[1]
    c = t1[2]
    d = t1[3]
    e = t1[4]
    f = t1[5]
    g = t1[6]
    h = t1[7]
    dtup = (a,b,c,d,e,f,g,h) # creating a tuple(immutable one dimensional array) with the letters from the text as elements
    print("Your original text was",''.join(dtup),'.') # '' stores what will separate the tuple charachters and .join() is used to print the tuple as a string.


validateInput(input("Enter the text with 8 chars:")) # calling the function with user input text passed as a parameter
t1 = list(validateInput.text) # creating a var t1 of list type from validateInput's text. Used in order to be able to manipulate individual charachters
encryptText() # calling the function
decryptText()

time.sleep(10) # stops compilation of code for 10 secs
os.system('cls') # clears the terminal window
sys.exit() # closes the terminal window
