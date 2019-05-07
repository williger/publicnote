# Publicnote
Public Encrypted Notes

Enter any title to access a note. No account required.

Every note is public. You are free to modify any note you see.

Every note is encrypted. You must know the title to see the note.

Publicnote is a zero-knowledge cloud notes app, where all user data is encrypted using AES256 and the encryption key is never exposed to the cloud.  The title to the note is used as the encryption key.  The title is hashed using SHA256 and used as an identifier for the data that is stored or retrieved.  The user's title is never exposed, thus neither the website owner nor AWS (where the data is stored) can view the plaintext context of the user's data (unless the title is easily guessed).

                            SHA256         
                    🔑title -----> identifier
                        | 
                        v 🔒
    user data -----> AES256 -----> cloud storage


Publicnote is both public and private.  Simple titles lead to highly visible notes that can be edited by the public, and complex titles lead to notes that are securly encrypted and private.  The more complex the title is, the stronger the encryption is.  

By design, there is no way to recover a note if you lose the title.  This is done to honor the user's privacy.

Publicnote is open source and offered as a free service, running thanks to your cryptocurrency donations.

daniel@ncrypt.org  
BTC: 1HrQfojcRt4gGEZntEwp24KVrSch8mtqMk  
LTC: Lc5Mw23SWYJjX3Fx4Nw7J5PG4eyyG3Pow2  
