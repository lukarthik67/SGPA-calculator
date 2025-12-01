```python
def calculate_sgpa():
    name = input("Enter your name: ")
    usn = input("Enter your USN: ")
    num_subjects = int(input("Enter the number of subjects: "))

    total_credits = 0
    total_weighted_score = 0

    for i in range(1, num_subjects + 1):
        marks = int(input(f"\nEnter marks scored in Subject {i}: "))

        if marks >= 90:
            grade_point = 10
        elif marks >= 80:
            grade_point = 9
        elif marks >= 70:
            grade_point = 8
        elif marks >= 60:
            grade_point = 7
        elif marks >= 50:
            grade_point = 6
        elif marks >= 40:
            grade_point = 5
        elif marks >= 30:
            grade_point = 4
        elif marks >= 20:
            grade_point = 3
        elif marks >= 10:
            grade_point = 2
        else:
            grade_point = 1

        credit = int(input(f"Enter credit of Subject {i}: "))
        total_credits += credit
        total_weighted_score += grade_point * credit

    if total_credits > 0:
        sgpa = total_weighted_score / total_credits
        print(f"\n{name} ({usn})")
        print(f"SGPA: {sgpa:.2f}")
    else:
        print("Invalid total credits. Please try again.")


calculate_sgpa()
```
#i updated
