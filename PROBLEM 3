class Employee:
    def __init__(self, employee_id, name, organization):
        self.employee_id = employee_id
        self.name = name
        self.organization = organization
        self.attendance = []  # List to track attendance (True = Present, False = Absent)

    def mark_attendance(self, present):
        self.attendance.append(present)

    def calculate_attendance_percentage(self):
        if not self.attendance:
            return 0.0
        return (sum(self.attendance) / len(self.attendance)) * 100

    def __str__(self):
        return f"ID: {self.employee_id}, Name: {self.name}, Organization: {self.organization}, Attendance: {self.attendance}"


class AttendanceTracker:
    def __init__(self):
        self.employees = []

    def add_employee(self, employee_id, name, organization):
        new_employee = Employee(employee_id, name, organization)
        self.employees.append(new_employee)
        print(f"Employee {name} added successfully.")

    def mark_attendance(self, employee_id, present):
        for employee in self.employees:
            if employee.employee_id == employee_id:
                employee.mark_attendance(present)
                status = "Present" if present else "Absent"
                print(f"Marked {status} for {employee.name}.")
                return
        print("Employee not found.")

    def display_all_attendance_records(self):
        if not self.employees:
            print("No employees found.")
            return
        for employee in self.employees:
            print(employee)

    def display_attendance_percentage(self):
        if not self.employees:
            print("No employees found.")
            return
        for employee in self.employees:
            percentage = employee.calculate_attendance_percentage()
            print(f"{employee.name} - Attendance Percentage: {percentage:.2f}%")


def main():
    tracker = AttendanceTracker()

    while True:
        print("\nEmployee Attendance Tracker")
        print("1. Add Employee")
        print("2. Mark Attendance")
        print("3. View All Attendance Records")
        print("4. Display Attendance Percentage")
        print("5. Exit")

        choice = input("Select an option (1-5): ")

        if choice == '1':
            employee_id = input("Enter Employee ID: ")
            name = input("Enter Employee Name: ")
            organization = input("Enter Organization Name: ")
            tracker.add_employee(employee_id, name, organization)

        elif choice == '2':
            employee_id = input("Enter Employee ID: ")
            present = input("Is the employee present? (yes/no): ").strip().lower() == 'yes'
            tracker.mark_attendance(employee_id, present)

        elif choice == '3':
            tracker.display_all_attendance_records()

        elif choice == '4':
            tracker.display_attendance_percentage()

        elif choice == '5':
            print("Exiting the program.")
            break

        else:
            print("Invalid option. Please try again.")


if __name__ == "__main__":
    main()
