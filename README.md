students = []

# Add a new student
def add_student():
    name = input("Enter student name: ")
    roll = input("Enter roll number: ")
    marks = float(input("Enter marks: "))
    student = {"name": name, "roll": roll, "marks": marks}
    students.append(student)
    print(f"Student {name} added successfully!\n")

# Display all student records
def display_students():
    if not students:
        print("No student records available.\n")
        return
    print("\n--- Student Records ---")
    for s in students:
        print(f"Name: {s['name']}, Roll: {s['roll']}, Marks: {s['marks']}")
    print()

# Search for a student by roll number
def search_student():
    roll = input("Enter roll number to search: ")
    found = False
    for s in students:
        if s["roll"] == roll:
            print(f"Found: Name: {s['name']}, Marks: {s['marks']}\n")
            found = True
            break
    if not found:
        print("Student not found.\n")

# Delete student by roll number
def delete_student():
    roll = input("Enter roll number to delete: ")
    for s in students:
        if s["roll"] == roll:
            students.remove(s)
            print("Student deleted.\n")
            return
    print("Student not found.\n")

# Update marks
def update_marks():
    roll = input("Enter roll number to update marks: ")
    for s in students:
        if s["roll"] == roll:
            new_marks = float(input("Enter new marks: "))
            s["marks"] = new_marks
            print("Marks updated successfully.\n")
            return
    print("Student not found.\n")

# Calculate average marks
def calculate_average():
    if not students:
        print("No records to calculate average.\n")
        return
    total = sum([s["marks"] for s in students])
    avg = total / len(students)
    print(f"Average Marks of all students: {avg:.2f}\n")

# Menu-driven interface
def menu():
    while True:
        print("1. Add Student")
        print("2. Display Students")
        print("3. Search Student")
        print("4. Delete Student")
        print("5. Update Marks")
        print("6. Calculate Average")
        print("7. Exit")
        choice = input("Enter your choice: ")
        
        if choice == "1":
            add_student()
        elif choice == "2":
            display_students()
        elif choice == "3":
            search_student()
        elif choice == "4":
            delete_student()
        elif choice == "5":
            update_marks()
        elif choice == "6":
            calculate_average()
        elif choice == "7":
            print("Exiting program.")
            break
        else:
            print("Invalid choice. Try again.\n")

# Start the program
menu()




