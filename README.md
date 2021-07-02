# Counting-Sort-Optimization

Constraints:
1. Input (an array to be sorted)
2. Number of element in input (n)
3. Keys in the range of 0..k-1 (k)
4. Count (an array of number)
Pseudocode:
for x in input:
 count[key(x)] += 1
total = 0
for i in range(k):
 oldCount = count[i]
 count[i] = total
 total += oldCount
 for x in input:
 output[count[key(x)]] = x
 count[key(x)] += 1
return output
