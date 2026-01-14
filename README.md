# Program: p1.py
## Date: January 14th 2026
### Author: Chris Pelletier 
### Description: This program reads the number of steps taken and the stridelength in inches. It calculates the miles walked and displays whether the user is under, over, or exactly at 10,000 steps.
# -------------------------
# input
### 1. Steps = 4200 Stride = 29 inches
### 2. Steps = 9800 Stride = 31 inches
### 3. Steps = 14500 Stride = 26 inches 
### 4. Steps = 10000 Stride = 24 inches 

# -------------------------
```python
print("Enter number of steps")
steps = int(input())
```
```python
print("Enter stride distance in inches")
stride = int(input())
```
# -------------------------
# processing

### 1. 4200 x 29 = 121,800 inches,  121,800 / 63,360 = 1.93 mi 
### 2. 9800 x 31 = 303,800 inches,  303,800 / 63,360 = 4.8 mi 
### 3. 14500 x 26 = 377,000 inches,  377,000 / 63,360 = 5.95 mi 
### 4. 10000 x 24 = 240,000 inches,  240,000 / 63,360 = 3.79 mi 

# -------------------------
# calculate total inches walked
total_inches = steps * stride

# convert inches to miles (63,360 inches = 1 mile)
miles = total_inches / 63360

# determine difference from 10,000 steps
difference = steps - 10000

# -------------------------
# output

### 1.  5,800 more steps needed to reach 10k
### 2.  200 more steps needed to reach 10k 
### 3.  4500 steps over 10k 
### 4.  10k steps walked exactly 

# -------------------------
# miles output (formatted to two decimals)
```python
print(f"You walked {steps:,} steps which is {miles:.2f} miles")
```
# step comparison output
```python
if steps < 10000:
    print(f"You need {abs(difference):,} more steps to reach 10,000")
elif steps > 10000:
    print(f"You were {difference:,} steps over 10,000")
else:
    print("You walked exactly 10,000 steps")
```
