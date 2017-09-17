This script enables the encryption and decryption of individual worksheets in a Google Sheet.

Installation: 
Open the script editor in your spreadsheet and insert a copy of Code.gs.

Usage: 
With the worksheet you want to encrypt selected, click Encryption / Encrypt sheet. You'll
be prompted for a key and an optional hint. Then a new worksheet will be created with the result 
of the encryption. You can then delete the unencrypted sheet, so that only the encrypted sheet is 
saved in the cloud. To get the original back, click Encryption / Decrypt sheet and enter the same
key as the one used to encrypt. If you forget the key used to encrypt the sheet, you will not be
able to decrypt the sheet.

Details: 
The contents of each cell in the sheet is concatenated into a long string which is then
encrypted using the well-regarded crypto-js library and stored in cell A3. If a hint is provided, 
it appears in cell A1 of the encrypted sheet. The rest of sheet contains data used to replicate
the original format.

Limitations:
Only the data in the sheet is preserved; any formulas are lost.

Used carefully, this code will keep data safe from a casual viewer. Although the encryption
itself is strong, the process of moving and storing data in the cloud can be exploited by a 
determined adversary. In particular, you should ensure that no plaintext is shown in the 
version history of the spreadsheet.
