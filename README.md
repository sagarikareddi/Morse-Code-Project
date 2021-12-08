# Morse-Code-Project
from functools import partial
from tkinter import *
import time

root = Tk()
root.geometry("902x700")
root.minsize(902, 700)
root.maxsize(902, 700)



# Function to clear text of result
def clearAll():
    # whole content of text area  is deleted
    result.delete(1.0, END)


# function to change morse code to alphabet or alphabet or sentence to morse code.
def morseCodeToAlphabet():
    converted_morse_code_to_alpha = ""
    code = morse_inputEntry.get()
    if code == ".-":
        converted_morse_code_to_alpha = "A"
    elif code == "-...":
        converted_morse_code_to_alpha = "B"
    elif code == "-.-.":
        converted_morse_code_to_alpha = "C"
    elif code == "-..":
        converted_morse_code_to_alpha = "D"
    elif code == ".":
        converted_morse_code_to_alpha = "E"
    elif code == "..-.":
        converted_morse_code_to_alpha = "F"
    elif code == "--.":
        converted_morse_code_to_alpha = "G"
    elif code == "....":
        converted_morse_code_to_alpha = "H"
    elif code == "..":
        converted_morse_code_to_alpha = "I"
    elif code == ".---":
        converted_morse_code_to_alpha = "J"
    elif code == "-.-":
        converted_morse_code_to_alpha = "K"
    elif code == ".-..":
        converted_morse_code_to_alpha = "L"
    elif code == "--":
        converted_morse_code_to_alpha = "M"
    elif code == "-.":
        converted_morse_code_to_alpha = "N"
    elif code == "---":
        converted_morse_code_to_alpha = "O"
    elif code == ".--.":
        converted_morse_code_to_alpha = "P"
    elif code == "--.-":
        converted_morse_code_to_alpha = "Q"
    elif code == ".-.":
        converted_morse_code_to_alpha = "R"
    elif code == "...":
        converted_morse_code_to_alpha = "S"
    elif code == "-":
        converted_morse_code_to_alpha = "T"
    elif code == "..-":
        converted_morse_code_to_alpha = "U"
    elif code == "...-":
        converted_morse_code_to_alpha = "V"
    elif code == ".--":
        converted_morse_code_to_alpha = "W"
    elif code == "-..-":
        converted_morse_code_to_alpha = "X"
    elif code == "-.--":
        converted_morse_code_to_alpha = "y"
    elif code == "--..":
        converted_morse_code_to_alpha = "Z"
    # Number Morse code
    elif code == ".----":
        converted_morse_code_to_alpha = "1"
    elif code == "..---":
        converted_morse_code_to_alpha = "2"
    elif code == "...--":
        converted_morse_code_to_alpha = "3"
    elif code == "....-":
        converted_morse_code_to_alpha = "4"
    elif code == ".....":
        converted_morse_code_to_alpha = "5"
    elif code == "-....":
        converted_morse_code_to_alpha = "6"
    elif code == "--...":
        converted_morse_code_to_alpha = "7"
    elif code == "---..":
        converted_morse_code_to_alpha = "8"
    elif code == "----.":
        converted_morse_code_to_alpha = "9"
    elif code == "-----":
        converted_morse_code_to_alpha = "0"
    # Symbols code
    elif code == ".-.-.-":
        converted_morse_code_to_alpha = "."
    elif code == "--..--":
        converted_morse_code_to_alpha = ","
    elif code == "..--..":
        converted_morse_code_to_alpha = "?"
    elif code == "-.-.--":
        converted_morse_code_to_alpha = "!"
    elif code == ".----.":
        converted_morse_code_to_alpha = "'"
    elif code == ".-..-.":
        converted_morse_code_to_alpha = '"'
    elif code == "-.--.":
        converted_morse_code_to_alpha = "("
    elif code == "-.--.-":
        converted_morse_code_to_alpha = ")"
    elif code == ".-...":
        converted_morse_code_to_alpha = "&"
    elif code == "---...":
        converted_morse_code_to_alpha = ":"
    elif code == "-.-.-.":
        converted_morse_code_to_alpha = ";"
    elif code == "-..-.":
        converted_morse_code_to_alpha = "/"
    elif code == "..--.-":
        converted_morse_code_to_alpha = "_"
    elif code == "-...-":
        converted_morse_code_to_alpha = "="
    elif code == ".-.-.":
        converted_morse_code_to_alpha = "+"
    elif code == "-....-":
        converted_morse_code_to_alpha = "-"
    elif code == "...-..-":
        converted_morse_code_to_alpha = "$"
    elif code == ".--.-.":
        converted_morse_code_to_alpha = "@"
    else:
        converted_morse_code_to_alpha = "Given morse code is wrong."
    result_code(converted_morse_code_to_alpha, code)


def AlphabetToMorseCode(slice_str):
    morse_code = ""
    if slice_str == 'pas':
        code = alpha_inputEntry.get()
    else:
        code = slice_str

    # Convert alphabet to Morse code by compression.

    if code == "A" or code == 'a':
        morse_code = ".-"
    elif code == "B" or code == 'b':
        morse_code = "-..."
    elif code == "C" or code == 'c':
        morse_code = "-.-."
    elif code == "D" or code == 'd':
        morse_code = "-.."
    elif code == "E" or code == 'e':
        morse_code = "."
    elif code == "F" or code == 'f':
        morse_code = "..-."
    elif code == "G" or code == 'g':
        morse_code = "--."
    elif code == "H" or code == 'h':
        morse_code = "...."
    elif code == "I" or code == 'i':
        morse_code = ".."
    elif code == "J" or code == 'j':
        morse_code = ".---"
    elif code == "K" or code == 'k':
        morse_code = "-.-"
    elif code == "L" or code == 'l':
        morse_code = ".-.."
    elif code == "M" or code == 'm':
        morse_code = "--"
    elif code == "N" or code == 'n':
        morse_code = "-."
    elif code == "O" or code == 'o':
        morse_code = "---"
    elif code == "P" or code == 'p':
        morse_code = ".--."
    elif code == "Q" or code == 'q':
        morse_code = "--.-"
    elif code == "R" or code == 'r':
        morse_code = ".-."
    elif code == "S" or code == 's':
        morse_code = "..."
    elif code == "T" or code == 't':
        morse_code = "-"
    elif code == "U" or code == 'u':
        morse_code = "..-"
    elif code == "V" or code == 'v':
        morse_code = "...-"
    elif code == "W" or code == 'w':
        morse_code = ".--"
    elif code == "X" or code == 'x':
        morse_code = "-..-"
    elif code == "Y" or code == 'y':
        morse_code = "-.--"
    elif code == "Z" or code == 'z':
        morse_code = "--.."
    # Number Morse code
    elif code == "1":
        morse_code = ".----"
    elif code == "2":
        morse_code = "..---"
    elif code == "3":
        morse_code = "...--"
    elif code == "4":
        morse_code = "....-"
    elif code == "5":
        morse_code = "....."
    elif code == "6":
        morse_code = "-...."
    elif code == "7":
        morse_code = "--..."
    elif code == "8":
        morse_code = "---.."
    elif code == "9":
        morse_code = "----."
    elif code == "0":
        morse_code = "-----"
    # Symbols code
    elif code == ".":
        morse_code = ".-.-.-"
    elif code == ",":
        morse_code = "--..--"
    elif code == "?":
        morse_code = "..--.."
    elif code == "!":
        morse_code = "-.-.--"
    elif code == "'":
        morse_code = ".----."
    elif code == '"':
        morse_code = ".-..-."
    elif code == "(":
        morse_code = "-.--."
    elif code == ")":
        morse_code = "-.--.-"
    elif code == "&":
        morse_code = ".-..."
    elif code == ":":
        morse_code = "---..."
    elif code == ";":
        morse_code = "-.-.-."
    elif code == "/":
        morse_code = "-..-."
    elif code == "_":
        morse_code = "..--.-"
    elif code == "=":
        morse_code = "-...-"
    elif code == "+":
        morse_code = ".-.-."
    elif code == "-":
        morse_code = "-....-"
    elif code == "$":
        morse_code = "...-..-"
    elif code == "@":
        morse_code = ".--.-."
    elif code == " ":
        morse_code = "\t"
    else:
        morse_code = "Error"
    # string_join(morse_code)
    result_code(morse_code, code)


def string_to_char():
    user_code = string_inputEntry.get()
    for index in user_code:
        AlphabetToMorseCode(index)


def result_code(conv_code, user_input):
    result.insert('end -1 chars', conv_code)


# ---------------------------------------------------------------------------------------------------------
# GUI FRAME START
str_pass = 'pas'
heading = Frame(root, borderwidth=5, bg="gray", relief=SUNKEN)
heading.pack(fill="x")

morsecode = Label(heading, text="Welcome To Morse Code Converter", font="Robot 15 bold", bg="gray")
morsecode.pack()

# Alphabet to morse code Frame
alphatomorse = Frame(root, borderwidth=5, bg="gray", relief=SUNKEN)
alphatomorse.place(x=1, y=40, height=400, width=300)
Label(alphatomorse, text="Alphabet To Morse Code").pack()

# Morse code to sentence Frame
morsetoalpha = Frame(root, borderwidth=5, bg="gray", relief=SUNKEN)
morsetoalpha.place(x=301, y=40, height=400, width=300)
Label(morsetoalpha, text="Morse Code To Alphabet").pack()

# sentence to morse code Frame
sentencetomorse = Frame(root, borderwidth=5, bg="gray", relief=SUNKEN)
sentencetomorse.place(x=601, y=40, height=400, width=300)
Label(sentencetomorse, text="Sentence To Morse Code").pack()

# Frame for text Encrypt
encr = Frame(root, borderwidth=5, bg="white", relief=SUNKEN)
encr.place(x=0, y=400, height=50, width=900)
Label(encr, text="Encrypted Data", bg="white", font="Robot 16 bold").place(x=400, y=0)
# Result Frame
result = Text(root, height=300, width=900, borderwidth=5, bg="white", relief=SUNKEN, font="robot 18")
result.place(x=0, y=440, height=300, width=900)

# alphabet to morse code frame - input
alpha_input = StringVar()
alpha_inputEntry = Entry(alphatomorse, textvariable=alpha_input)
alpha_inputEntry.place(x=20, y=80, height=20, width=250)
alpha_input_button = Button(alphatomorse, text="Encrypt", command=partial(AlphabetToMorseCode, str_pass)).place(x=80, y=110)
clearBtn1 = Button(alphatomorse, text="Clear Result", command=clearAll).place(x=160, y=110)
line1 = Label(alphatomorse, text="---------------------------------------------------------", bg="gray").place(x=0, y=250)

# morse code to alphabet frame - input
morse_input = StringVar()
morse_inputEntry = Entry(morsetoalpha, textvariable=morse_input)
morse_inputEntry.place(x=20, y=80, height=20, width=250)
morse_input_button = Button(morsetoalpha, text="Decrypt", command=morseCodeToAlphabet).place(x=80, y=110)
clearBtn2 = Button(morsetoalpha, text="Clear Result", command=clearAll).place(x=160, y=110)
line2 = Label(morsetoalpha, text="---------------------------------------------------------", bg="gray").place(x=0, y=250)

# String to morse code frame - input
string_input = StringVar()
string_inputEntry = Entry(sentencetomorse, textvariable=string_input)
string_inputEntry.place(x=20, y=80, height=20, width=250)
string_input_button = Button(sentencetomorse, text="Encrypt", command=string_to_char).place(x=80, y=110)
clearBtn3 = Button(sentencetomorse, text="Clear Result", command=clearAll).place(x=160, y=110)
line3 = Label(sentencetomorse, text="---------------------------------------------------------", bg="gray").place(x=0, y=250)

root.mainloop()
