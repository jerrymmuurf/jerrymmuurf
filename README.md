numbers = [5, 12, 7, 18, 9, 24, 3, 16, 11]

div_by_3 = 0
even_not_3 = 0
odd_not_3 = 0

for num in numbers:
    if num % 3 == 0:
        print(f"{num} is divisible by 3")
        div_by_3 += 1
    elif num % 2 == 0:
        print(f"{num} is even but not divisible by 3")
        even_not_3 += 1
    else:
        print(f"{num} is odd and not divisible by 3")
        odd_not_3 += 1

print(f"\nDivisible by 3: {div_by_3}")
print(f"Even but not divisible by 3: {even_not_3}")
print(f"Odd and not divisible by 3: {odd_not_3}")


