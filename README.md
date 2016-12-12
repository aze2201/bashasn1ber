# bashasn1ber

ASN.1 Abstract Syntax Notation One (ASN.1) is a standard and notation that describes rules and structures for representing, encoding, transmitting, and decoding data in telecommunications and computer networking. The formal rules enable representation of objects that are independent of machine-specific encoding techniques. Formal notation makes it possible to automate the task of validating whether a specific instance of data representation abides by the specifications. In other words, software tools can be used for the validation

More information https://en.wikipedia.org/wiki/Abstract_Syntax_Notation_One

BER The format for Basic Encoding Rules specifies a self-describing and self-delimiting format for encoding ASN.1 data structures. Each data element is encoded as a type identifier, a length description, the actual data elements, and, where necessary, an end-of-content marker. These types of encodings are commonly called type-length-value or TLV encodings. This format allows a receiver to decode the ASN.1 information from an incomplete stream, without requiring any pre-knowledge of the size, content, or semantic meaning of the data

More information https://en.wikipedia.org/wiki/X.690#BER_encoding

THIS SCRIPT WILL HELP TO DECODE ASN1 BER encoded files. 1. put anyplace on Linux machine which is support openssl and run by below command ./ASN1.BER -f <filename>                  # full decode, WARNING: if you decode full file it can be take long time due for bash commands 
./ASN1.BER -f <filename> -b 10 -e 15      # it will decode from offset 10 till 15

If you have file structure description you can refer for covert field values to ASCII or DEC etc.



EXAMPLE: test:asntmp # ./ASN1.BER -f file -b 10 -e 15

----- OFFSET= 46 (Tag) 8 (Length) 2 ( Value ) = 021
----- OFFSET= 50 (Tag) 9 (Length) 8 ( Value ) = a00f31dcb
---------- OFFSET= 52 (Tag) 0 (Length) 6 ( Value ) = 8004a
--------------- OFFSET= 54 (Tag) 0 (Length) 4 ( Value ) = 0af31
----- OFFSET= 60 (Tag) 11 (Length) 1 ( Value ) = ff
----- OFFSET= 63 (Tag) 12 (Length) 34 ( Value ) = 3020830304631b840304612062149392b0400a90 

test:asntmp #
