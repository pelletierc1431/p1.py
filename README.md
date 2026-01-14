# Program: p1.py
## Date: January 14th 2026
### Author: Chris Pelletier 
### Description: This program reads the number of steps taken and the stridelength in inches. It calculates the miles walked and displays whether the user is under, over, or exactly at 10,000 steps.

# -------------------------
# input
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
# -------------------------

# total inches walked
total_inches = steps * stride

# convert inches to miles (63,360 inches = 1 mile)
miles = total_inches / 63360

# determine difference from 10,000
difference = steps - 10000

# -------------------------
# output
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
