package package1;

public class SumOfOddNumbers { public static void main(String[]args) { int sum=0;

 for(int i=7;i<=21;i++)
 {
	 if(i%2!=0)
	 {
		sum=sum+i; 
	 }
 }
 System.out.println("sum of odd numbers between 7 to 21 is:"+sum);
} }

===========================================================================================================

package pack1;

import java.util.Scanner;

public class StudentGrades { public static void main(String[] args) { Scanner scanner = new Scanner(System.in); String[] studentNames = new String[10]; double[] attendancePercentages = new double[10];

    for (int i = 0; i < 10; i++) {
        System.out.print("Enter the name of student " + (i + 1) + ": ");
        studentNames[i] = scanner.nextLine();
        System.out.print("Enter the attendance percentage for " + studentNames[i] + ": ");
        attendancePercentages[i] = scanner.nextDouble();
        scanner.nextLine(); 
    }

    System.out.println("Student Grades:");
    for (int i = 0; i < 10; i++) {
        System.out.print(studentNames[i] + ": ");
        char grade;

        
        switch ((int) attendancePercentages[i] / 10) {
            case 9:
            case 10:
                grade = 'A';
                break;
            case 8:
                grade = 'B';
                break;
            case 7:
                grade = 'C';
                break;
            case 6:
                grade = 'D';
                break;
            default:
                grade = 'E';
                break;
        }

        System.out.println(grade);
    }
}
}

=========================================================================================================

package Package1; import java.util.Scanner;

public class characterString { static String CharactersString(String input) { char[] chars = input.toCharArray(); for (int i = 0; i < chars.length; i++) { char c = chars[i]; if (Character.isUpperCase(c)) { chars[i] = (char) (((c - 'A' - 2 + 26) % 26) + 'A'); //upper case letters by 2 characters } else if (Character.isLowerCase(c)) { chars[i] = (char) (((c - 'a' - 3 + 26) % 26) + 'a'); //lower case letters by 3 characters } } return new String(chars); }

public static void main(String[] args) { Scanner sc = new Scanner(System.in); System.out.print("Enter a string: "); String input = sc.nextLine(); String characters = CharactersString(input); System.out.println("Shifted string: " + characters); } }

O/P;

Enter a string: "Hello" Shifted string: "Fbiil"
