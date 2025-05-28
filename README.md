def classify_numbers(numbers):
    counts = {"positive": 0, "zero": 0, "negative": 0}

    for num in numbers:
        if num > 0:
            print(f"{num} is positive")
            counts["positive"] += 1
        elif num == 0:
            print(f"{num} is zero")
            counts["zero"] += 1
        else:
            print(f"{num} is negative")
            counts["negative"] += 1

    return counts

# Example
nums = [-5, 0, 3, 9, -1, 0, 7]
summary = classify_numbers(nums)
print("Counts:", summary)
-5 is negative
0 is zero
3 is positive
9 is positive
-1 is negative
0 is zero
7 is positive
Counts: {'positive': 3, 'zero': 2, 'negative': 2}



