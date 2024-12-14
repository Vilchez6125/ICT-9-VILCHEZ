class StudentGrades:
    def __init__(self):
        self.students = {}

    def add_student(self, name, student_id, course, grade1, grade2, grade3, grade4):
        """Add a new student with their grades."""
        self.students[name] = {
            'student_id': student_id,
            'course': course,
            'grades': [grade1, grade2, grade3, grade4]
        }
        print(f"Added student: {name} {student_id} {course} with grades: {grade1}, {grade2}, {grade3}, {grade4}")

    def update_grade(self, name, new_grade1, new_grade2, new_grade3, new_grade4):
        """Update the grades of an existing student."""
        if name in self.students:
            self.students[name]['grades'] = [new_grade1, new_grade2, new_grade3, new_grade4]
            print(f"Updated {name}'s grades to: {new_grade1}, {new_grade2}, {new_grade3}, {new_grade4}")
        else:
            print(f"Student {name} not found.")

    def display_students(self):
        """Display all students and their grades."""
        if not self.students:
            print("No students found.")
            return
        print("Students and their grades:")
        for name, info in self.students.items():
            grades = info['grades']
            print(f"{name} {info['student_id']} {info['course']} English: {grades[0]} Science: {grades[1]} Math: {grades[2]} Filipino: {grades[3]}")

    def calculate_average(self):
        """Calculate and display the class average grade."""
        if not self.students:
            print("No students to calculate average.")
            return
        total_grades = 0
        total_subjects = 0
        for info in self.students.values():
            total_grades += sum(info['grades'])
            total_subjects += len(info['grades'])
        average = total_grades / total_subjects if total_subjects > 0 else 0
        print(f"Class average grade: {average:.2f}")


def main():
    student_grades = StudentGrades()

    while True:
        print("\nMenu:")
        print("1. Add a new student")
        print("2. Update a student's grade")
        print("3. Display all students and their grades")
        print("4. Calculate and display the class average grade")
        print("5. Exit")

        choice = input("Enter your choice (1-5): ")

        if choice == '1':
            name = input("Enter student's name: ")
            student_id = input("Enter student id: ")
            course = input("Enter student course: ")
            grade1 = float(input("Enter student's grade in English: "))
            grade2 = float(input("Enter student's grade in Science: "))
            grade3 = float(input("Enter student's grade in Math: "))
            grade4 = float(input("Enter student's grade in Filipino: "))
            student_grades.add_student(name, student_id, course, grade1, grade2, grade3, grade4)
        elif choice == '2':
            name = input("Enter student's name to update: ")
            new_grade1 = float(input("Enter new grade in English: "))
            new_grade2 = float(input("Enter new grade in Science: "))
            new_grade3 = float(input("Enter new grade in Math: "))
            new_grade4 = float(input("Enter new grade in Filipino: "))
            student_grades.update_grade(name, new_grade1, new_grade2, new_grade3, new_grade4)
        elif choice == '3':
            student_grades.display_students()
        elif choice == '4':
            student_grades.calculate_average()
        elif choice == '5':
            print("Exiting the program.")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
