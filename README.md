# Java-Kullan-c-girisiprogram-
Java-Kullanıcıgirisiprogramı

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        String userName, password, newPassword;
        int secim;

        Scanner inp = new Scanner(System.in);

        System.out.print("Kullanıcı Adınız : ");
        userName = inp.nextLine();

        System.out.print("Şifreniz : ");
        password = inp.nextLine();

        if (userName.equals("inci") && password.equals("inci123")){
            System.out.println("Giriş Yaptınız!");
        }else if (!password.equals("inci123")){
            System.out.println("Şifreniz hatalı!");
            System.out.println("Şifrenizi sıfırlamak ister misiniz?\\nİstemezseniz -1\nİsterseniz -2");
            secim = inp.nextInt();
            switch (secim){
                case 1:
                    System.out.println("İşleminiz sonlandırıldı : ");
                    break;
                case 2:
                    System.out.print("Yeni şifrenizi giriniz : ");
                    newPassword = inp.next();
                    if (!password.equals(newPassword)) {
                        System.out.print("Şifreniz başarıyla oluşturuldu.");
                    } else {
                        System.out.println("Şifreniz oluşturulamadı.Tekrar deneyiniz!");
                    }
                     break;
                default:
            }

        }
    }
}

