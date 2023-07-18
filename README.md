#Update
Used AI Tools to rectify the issues faced initially in the code. 
Will be using a different approach to continue the same

#Update2
Will try using C Language and import the grain module (not available as an open source) using GitHub Repos

#Update3 
Working on Issue 2

The Grain Cipher Implementation involves the encryption of data using functions of Linear Feedback Shift Registers.
It has two shift registers, LFSR and NFSR. 
It will focus on generating a keystream corresponding to the given initialization vector, key, and plain text.

#OUTLINE of the Key Stream
The key represented by the key1 array in hex format is:

01 23 45 67 89 AB CD EF 12 34 --> This is the constant key in hex form. 

Each element in the key1 array corresponds to one byte (8 bits) of the key. 

The key (key1 array) remains constant for all the iterations of the loop. Only the IVs are randomly generated for each iteration, and the corresponding keystream is computed based on that constant key and the generated IVs.

Since the key is the same (key1 array), the keystreams generated for different IVs will be different, allowing you to collect 10,000 unique IVs and their corresponding keystreams in the IV and keystream2 arrays, respectively. These values are then stored in the CSV file (data.csv) using the transferDataToCSV function.
