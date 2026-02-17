import java.util.Scanner;

class Student {

    // Final variable for course name
    final String COURSE_NAME = "Data Science";

    // Static variable to track total students
    static int totalStudents = 0;

    // Instance variables
    String name;
    int id;
    double marks;
    char grade;

    // Default constructor
    Student() {
        name = "Unknown";
        id = 0;
        marks = 0.0;
        grade = 'F';
        totalStudents++;
    }

    // Parameterized constructor
    Student(String name, int id, double marks) {
        this.name = name;
        this.id = id;
        this.marks = marks;
        this.grade = calculateGrade(marks);
        totalStudents++;
    }

    // Method to calculate grade
    char calculateGrade(double marks) {
        if (marks >= 90)
            return 'A';
        else if (marks >= 75)
            return 'B';
        else if (marks >= 60)
            return 'C';
        else if (marks >= 50)
            return 'D';
        else
            return 'F';
    }

    // Method to display student details
    void displayDetails() {
        System.out.println("\nCourse Name: " + COURSE_NAME);
        System.out.println("Student Name: " + name);
        System.out.println("Student ID: " + id);
        System.out.println("Marks: " + marks);
        System.out.println("Grade: " + grade);
    }
}

public class StudentPerformance {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of students: ");
        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        Student[] students = new Student[n];

        for (int i = 0; i < n; i++) {
            System.out.println("\nEnter details for Student " + (i + 1));

            System.out.print("Name: ");
            String name = sc.nextLine();

            System.out.print("ID: ");
            int id = sc.nextInt();

            System.out.print("Marks: ");
            double marks = sc.nextDouble();
            sc.nextLine(); // consume newline

            students[i] = new Student(name, id, marks);
        }

        // Display all student details
        System.out.println("\n--- Student Performance Details ---");
        for (Student s : students) {
            s.displayDetails();
        }

        // Display total students
        System.out.println("\nTotal Students: " + Student.totalStudents);

        sc.close();
    }
}
