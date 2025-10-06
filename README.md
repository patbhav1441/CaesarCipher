
For the Micro-Credential offered for this exercise. I had to write this sentence.
This is Caesar Cipher - a simple code that encrypts a message. This program shifts the character of a word, however many places the user wants to. And the shifting of the places is the key which can be used to decrypt the message. 



# CaesarCipher
Created a Caesar Cipher using python

text = 'Hello Zaira'
shift = 3

def caesar(message, offset):
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)

caesar(text, shift)
