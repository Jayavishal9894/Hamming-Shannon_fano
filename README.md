# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
google colab
# Program:
```
import numpy as np
import math
L = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range(n):
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))
    p.append(pr)
for j in range(n):
    l = float(input(f"Enter the length of the sample values {j + 1}: "))
    lk.append(l)
for k in range(n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
for k in range(n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs, 3)
eff = hs / L
eff = round(eff, 3)
red = round(1 - eff, 3)
var = 0
for k in range(n):
    var1 = p[k] * (lk[k] - L) ** 2
    var = var + var1
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
 
```
# Calculation:

<img width="498" height="832" alt="Screenshot 2025-09-12 204031" src="https://github.com/user-attachments/assets/b934ce19-91ed-481e-9950-b5553c575687" />

<img width="496" height="833" alt="Screenshot 2025-09-12 204040" src="https://github.com/user-attachments/assets/d0f9a152-07f3-4044-997c-15a6d1b05212" />

# Output
<img width="607" height="501" alt="Screenshot 2025-09-12 142419" src="https://github.com/user-attachments/assets/773ca79f-f5ee-45e3-b061-068ac7bcef8a" />

# Results:
Huffman and Shannon-Fano coding methods were implemented on the provided source. Calculations for average codeword length, entropy, variance, redundancy, and coding efficiency have been carried out successfully

