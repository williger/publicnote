# Publicnote
Public Encrypted Notes

Publicnote is a database of notes that is accessible to the public.  No account is required.  Simply enter a title to access any note.

Every note is encrypted with AES256, using the title as the encryption key.  A SHA256 hash of the title is used to index the encrypted note. The title is never exposed, thus neither the website owner nor AWS (where the data is stored) can view the plaintext contents of the note (unless the title is easily guessed).

Notes stored on publicnote can be public or private, depending on the complexity of the title. Simple titles lead to highly visible notes that can be edited by the public, and complex titles lead to private notes that are securely encrypted. The more complex the title is, the stronger the encryption is.

            title → SHA256 → index
             ⇣
             🔑
    note → AES256 → encrypted note

By design, there is no way to recover a note if you lose the title. This is done to honor the user's privacy.

Publicnote is open source and offered as a free service, running thanks to your cryptocurrency donations.

daniel@ncrypt.org
BTC: 1HrQfojcRt4gGEZntEwp24KVrSch8mtqMk  
LTC: Lc5Mw23SWYJjX3Fx4Nw7J5PG4eyyG3Pow2  
