# opp-week-4
oop week 4
//1.soru
import java.util.InputMismatchException;
import java.util.Scanner;

public class LabExerciseOne {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Bir tam sayı giriniz: ");
            int x = scanner.nextInt();
            System.out.println(x);
        } catch (InputMismatchException e) {
            System.out.println("Hata: Geçerli bir tam sayı girmediniz.");
        }

        scanner.close();
    }
}

// 2.soru
// app

public class App {
    public static void main(String[] args) {
        Worker worker1 = new Worker();
        Worker worker2 = new Worker();
        Worker worker3 = new Worker();

        worker1.SetSalary(-1);  // exception side
    }
}

//worker

public class Worker {

    private String name;
    private float salary;
    public static int counter = 0;

    public Worker()
    {
        counter++;
        System.out.println("Total worker count = " + counter);
    }

    public void SetSalary(float value)
    {
        if(value > 0)
            this.salary = value;
        else
            System.out.println("Salary amount must be greater than zero");
    }

    public void SetName(String value)
    {
        this.name = value;
    }
}
