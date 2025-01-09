# Task2-Password-Generator

import random
import string

def generate_password():
  
    characters = string.ascii_letters + string.digits
    
    try:
        length = int(input("Enter Length Of The Password: "))
        if length <= 0:
            raise ValueError("Length must be positive")
            
        password = ''.join(random.choice(characters) for _ in range(length))
        print("YOUR GENERATED PASSWORD IS:", password)
        return password
        
    except ValueError as e:
        print("Please enter a valid positive number")
        return None

if __name__ == "__main__":
    generate_password()
