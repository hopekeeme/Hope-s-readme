def collect_student_data():
    num_students = int(input("Enter the number of students: "))  # Prompt user for the number of students
    students = []  # Initialize an empty list to store student data
    
    for _ in range(num_students):  # Loop to gather data for each student
        name = input("Enter the student's name: ")  # Get student name
                grade = float(input(f"Enter {name}'s grade (0-100): "))  # Get and validate student's grade
                if 0 <= grade <= 100:  # Check if grade is within valid range
                    break  # Exit loop if grade is valid
                else:
                    print("Grade must be between 0 and 100.")  # Inform user of invalid grade
                   students.append((name, grade))  # Add the student's data to the list
    return students  # Return the list of students

2. Grade Calculation
def calculate_grades(students):
    total = sum(grade for _, grade in students)  # Calculate the total of all students' grades
    average = total / len(students) if students else 0     # Calculate the average grade
    return total, average  # Return total and average grades
   
4. Basic Validation
for name, grade in students: # Print each student's name and grade
    print(f"Student: {name}, Grade: {grade}")
print(f"Class Average: {average:.2f}") # Print the overall class average
