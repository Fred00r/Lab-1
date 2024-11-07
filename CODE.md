        import java.io.PrintStream;
        import java.util.Scanner;
        public class Main {
            public static Scanner in = new Scanner(System.in);
            public static PrintStream out = System.out;
            public static void main(String[] args) {
        // Вводим данные
                int a = in.nextInt();
                int b = in.nextInt();
                int c = in.nextInt();
                int d = in.nextInt();

        // Описываем условие ввода (точнее условие, при котором не осуществляется ввод)
                if ( a==b || a==c || a==d || b==c || b==d || c==d) {
                    out.print("Нарушено условие, неверный ввод!");
                }
        // Описываем поочерёдно 4 сложных условия
                else if ((a < b && a > c && a > d) || (a < c && a > b && a > d) || (a < d && a > b && a > c)) {
                    out.print(a);
                }
                else if ((b < a && b > c && b > d) || (b < c && b > a && b > d) || (b < d && b > a && b > c)) {
                    out.print(b);
                }
                else if ((c < a && c > b && c > d) || (c < b && c > a && c > d) || (c < d && c > a && c > b)) {
                    out.print(c);
                }    
                else if  ((d < a && d > b && d > c) || (d < b && d > a && d > c) || (d < c && d > a && d > b)) {
                    out.print(d);
                }
            }
        }
