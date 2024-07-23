import string
import random

def generate_password(length):
    # Define the characters to be used in the password
    characters = string.ascii_letters + string.digits + string.punctuation
    
    # Generate a random password
    password = ''.join(random.choice(characters) for i in range(length))
    
    return password

def main():
    try:
        # Prompt the user to specify the desired length of the password
        length = int(input("Enter the desired length of the password: "))
        
        if length < 1:
            raise ValueError("Length must be a positive integer.")
        
        # Generate the password
        password = generate_password(length)
        
        # Display the generated password
        print("Generated password:", password)
    except ValueError as ve:
        print("Invalid input:", ve)

if _name_ == "_main_":
    main()
