
# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.

# Tools Required:
* Python IDE with Numpy and Scipy Libraries

# Program:
```
import math

n = int(input("Enter number of samples: "))

p  = [float(input(f"Enter the Probability of sample value {i+1}: ")) for i in range(n)]
lk = [float(input(f"Enter the Length of sample value {i+1}: ")) for i in range(n)]

# Average codeword length
L = sum(p[i] * lk[i] for i in range(n))

# Entropy
hs = sum(p[i] * math.log(1/p[i], 2) for i in range(n))
hs = round(hs, 3)

# Efficiency and Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)

# Variance
var = sum(p[i] * (lk[i] - L)**2 for i in range(n))
var = round(var, 3)

print("Average Codeword Length:", L)
print("Entropy:", hs)
print("Efficiency:", eff)
print("Redundancy:", red)
print("Variance:", var)
```
# Calculation:
<img width="515" height="646" alt="image" src="https://github.com/user-attachments/assets/2e635c42-d083-4741-b4ce-b87298c56557" />

<img width="569" height="640" alt="image" src="https://github.com/user-attachments/assets/c8ec1e1d-88b9-4c2e-a573-d08cd44e9d35" />


# Output
<img width="1014" height="780" alt="image" src="https://github.com/user-attachments/assets/d8ddf512-1416-4847-aad2-e1c1c770226f" />



# Results:

Huffman and Shannon-Fano coding methods were implemented on the provided source. Calculations for average codeword length, entropy, variance, redundancy, and coding efficiency have been carried out successfully.
