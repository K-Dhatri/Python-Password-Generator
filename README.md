# Python-Password-Generator
 Generate strong and secure passwords with Python for your accounts.
import random
import string

def generate_password(length=12):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

if __name__ == "__main__":
    password_length = int(input("Enter the length of the password: "))
    generated_password = generate_password(password_length)
    print("Generated password:", generated_password)
Explanation:

import random: Import the random module to generate random numbers.
import string: Import the string module to get access to different sets of characters (letters, digits, punctuation).
def generate_password(length=12): Define a function generate_password that generates a random password. It takes an optional argument length which specifies the length of the password (default is 12 characters).
characters = string.ascii_letters + string.digits + string.punctuation: Define a string characters that contains all letters (both lowercase and uppercase), digits, and punctuation marks. This string will be used to generate the random password.
password = ''.join(random.choice(characters) for _ in range(length)): Generate a random password by randomly choosing characters from the characters string length times. random.choice(characters) randomly selects a character from the characters string, and ''.join(...) concatenates these characters together into a single string.
return password: Return the generated password.
if __name__ == "__main__":: This line checks if the script is being run directly (as opposed to being imported as a module). This allows us to execute code only when the script is run directly.
password_length = int(input("Enter the length of the password: ")): Prompt the user to enter the desired length of the password and convert the input to an integer.
generated_password = generate_password(password_length): Call the generate_password function with the specified password length and store the generated password in the variable generated_password.
print("Generated password:", generated_password): Print the generated password to the console.
