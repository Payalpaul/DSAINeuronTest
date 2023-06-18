Question: Given a non-negative integer x, return the square root of x rounded down to the nearest integer. The returned integer should be non-negative as well. You must not use any built-in exponent function or operator. 


Answer:

def mySqrt(x):
    if x == 0:
        return 0
    
    left = 1
    right = x
    
    while left <= right:
        mid = left + (right - left) 
        
        if mid * mid == x:
            return mid
        elif mid * mid < x:
            left = mid + 1
        else:
            right = mid - 1
    
    return right

x = 4
print(mySqrt(x))

x = 8
print(mySqrt(x))  
