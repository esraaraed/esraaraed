from Crypto.Cipher import AES
from Crypto.Util import Counter
import binascii
import os

matrix = [
    [5, 355, 637, 986, 323],
    [779, 797, 688, 856, 77],
    [182, 242, 888, 451, 396],
    [184, 418, 368, 80, 704],
    [196, 190, 313, 752, 60]
]

result = [
    [71, 420, 722, 1109, 390],
    [858, 907, 791, 970, 174],
    [298, 364, 983, 540, 444],
    [301, 513, 445, 177, 804],
    [247, 285, 418, 868, 185]
]

def getflag():
    combined_result = [] 
    for i in range(len(matrix)):
        row = []
        for j in range(len(matrix[0])):
            row.append(matrix[i][j] - result[i][j])
        combined_result.append(row)  
    return combined_result

row = getflag()  
print("Combined row:")
print(row) 
combined_row = [[-66, -65, -85, -123, -67],
                [-79, -110, -103, -114, -97],
                [-116, -122, -95, -89, -48],
                [-117, -95, -77, -97, -100],
                [-51, -95, -105, -116, -125]]

flag_prefix = "BAU"  # The desired prefix of the flag

flag = flag_prefix  # Start with the known prefix

# Convert each negative integer in the combined row to its corresponding ASCII character
for row in combined_row:
    for num in row:
        flag += chr(abs(num))  # Convert the negative number to its absolute value and then to a character

print("Flag:", flag)

#BAU{COngratz_Y0u_Mad3_it}
