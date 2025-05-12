## EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER
 

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


PROGRAM :-
~~~
def caesar_encrypt(text, key):
    encrypted_text = ""
    for char in text:
        if 'A' <= char <= 'Z':
            encrypted_text += chr(((ord(char) - ord('A') + key) % 26) + ord('A'))
        elif 'a' <= char <= 'z':
            encrypted_text += chr(((ord(char) - ord('a') + key) % 26) + ord('a'))
        else:
            encrypted_text += char  # Keep non-alphabetic characters unchanged
    return encrypted_text

def caesar_decrypt(text, key):
    return caesar_encrypt(text, -key)  # Decryption is the same as encryption with a negative key

if __name__ == "__main__":
    message = input("Enter the message to encrypt: ")
    key = int(input("Enter the Caesar Cipher key (an integer): "))
    
    encrypted_message = caesar_encrypt(message, key)
    print("Encrypted Message:", encrypted_message)
    
    decrypted_message = caesar_decrypt(encrypted_message, key)
    print("Decrypted Message:", decrypted_message)
~~~

OUTPUT :-
Simulating Caesar Cipher

![Screenshot 2025-03-19 084235](https://github.com/user-attachments/assets/ec4c7b79-c0c1-4374-bea6-3ee66670dd17)

Input : Anna University
Encrypted Message : Dqqd Xqlyhuvlwb Decrypted Message : Anna University

## RESULT:
The program is executed successfully
