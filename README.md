# Faktoriyel-hesaplama-programi
import java.util.Scanner;

public class Main {
    public static int faktoriyel(int sayi) {
        int sonuc = 1;
        for (int i = 1; i <= sayi; i++) {
            sonuc *= i;
        }
        return sonuc;
    }

    public static int kombinasyon(int n, int r) {
        return faktoriyel(n) / (faktoriyel(r) * faktoriyel(n - r));
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("n değerini girin: ");
        int n = scanner.nextInt();
        System.out.print("r değerini giriniz: ");
        int r = scanner.nextInt();

        if (n >= r && n > 0 && r >= 0) {
            System.out.println("C(" + n + "," + r + ") = " + kombinasyon(n, r));
        } else {
            System.out.println("Geçersiz değerler.");
        }
        scanner.close();
    }
}
