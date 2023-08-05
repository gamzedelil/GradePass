# GradePass

package gradepass;

import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		
		int math, physics, turkish, chemistry, music, lesson = 5;
		
		Scanner input = new Scanner(System.in);
		
		System.out.println("Enter the Math grade:");
		math = input.nextInt();
		
		System.out.println("Enter the Physics grade:");
		physics = input.nextInt();

		System.out.println("Enter the Turkish grade:");
		turkish = input.nextInt();

		System.out.println("Enter the Chemistry grade:");
		chemistry = input.nextInt();

		System.out.println("Enter the Music grade:");
		music = input.nextInt();
		
	     	if (math < 0 || math > 100) {
            math = 0;
            lesson--;
        }

        if (physics < 0 || physics > 100) {
            physics = 0;
            lesson--;
        }

        if (turkish < 0 || turkish > 100) {
            turkish = 0;
            lesson--;
        }

        if (chemistry < 0 || chemistry > 100) {
            chemistry = 0;
            lesson--;
        }

        if (music < 0 || music > 100) {
            music = 0;
            lesson--; 
        }
		
		double average = (math + physics + turkish + chemistry + music) / lesson; 
		
		if (average < 55 ) {
			System.out.println("You failed the class");
			System.out.println ("Your average is:" +average); 
		}
		
		else {
			System.out.println("You passed the class.");
			System.out.println ("Your average is:" +average); 
		}

	}

}
