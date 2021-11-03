import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

class Main{

    private String[] MyKelinci = {"Holland Lop","Netherland Dwarf"};
    public List <Kelinci> jenisSnack = new ArrayList<snack>();
    public List <Kelinci> jenisSnack2 = new ArrayList<snack>();

    public static void main(String[] args) {

        System.out.println("===================================================");
        System.out.println("\t\tJenis - jenis snack");
        System.out.println("===================================================");

        Scanner myObj = new Scanner(System.in);
        Main m = new Main();

        System.out.println("\nPilihlah angka untuk melanjutkan");
        System.out.println("1. Menambahkan jenis brownies ");
        System.out.println("2. Melihat jenis brownies");
        System.out.print("\nPilih angka : ");

        String input = myObj.nextLine();
        int code = Integer.parseInt(input);
        System.out.println("===================================================");

        switch (code) {
            case 1:
                m.InputListBrownies();
                break;
            case 2:
                m.ShowListBrownies();
                break;

            default:
                System.out.println("Pilihan tidak terdaftar");
                break;
        }

    }

    public void InputListBrownies(){

        System.out.println("\n---------------------------------------------------");
        System.out.println("\t\tMenambahkan Brownies");
        System.out.println("---------------------------------------------------\n");
        System.out.println("Pilih jenis Brownies : ");

        int i=1;
        for (String Brownies : Brownies){
            System.out.println(i + "." + Brownies);
            i++;
        }

        System.out.print("\nMasukkan pilihan : ");
        Scanner myObj = new Scanner(System.in);

        String inputProduct = myObj.nextLine();
        int product = Integer.parseInt(inputProduct);

        switch (product) {
            case 1:
                try {
                    jenisBrownies =  InputBrowniesiHl();
                } catch (Exception e) {
                    System.out.println("Masukkan data yang valid!");
                    System.out.println("Error: "+e.getMessage());
                }
                break;

            case 2:
                try {
                    jenisBrownies2 =  InputBrowniesND();
                } catch (Exception e) {
                    System.out.println("Masukkan data yang valid!");
                    System.out.println("Error: "+e.getMessage());
                }
                break;

            default:
                break;

        }

        myObj.close();

    }

    public List InputBrowniesHL() {

        Scanner myObj = new Scanner(System.in);
        System.out.println("\n============= Jenis Brownies baru =============");

        int jmlData1 = 2;
        for (int i = 0; i < jmlData1; i++) {
           Brownies k1 = new Brownies();
            System.out.println("Jenis ke-" + (i+1) + " :");

            System.out.print("Pilihan Rasa : ");
            String Rasa = myObj.nextLine();
            k1.setRasa(rasa);

            System.out.print("Bentuk Kemasan : ");
            String kemasan = myObj.nextLine();
            k1.setKemasan(kemasan);

            System.out.print("Warna Kemasan : ");
            String warna = myObj.nextLine();
            k1.setWarna(warna);

            System.out.println('\n');
            this.jenisBrownies1.add(k1);
        }

        System.out.println("\n");
        myObj.close();
        return this.jenisBrownies1;

    }

    public List InputBrowniesND() {

        Scanner myObj = new Scanner(System.in);
        System.out.println("\n============= Jenis Brownies Baru =============");

        int jmlData2 = 2;
        for (int i = 0; i < jmlData2; i++) {
           Snack k2 = new Brownies();
            System.out.println("Jenis ke-" + (i+1) + ":");

            System.out.print("Pilihan rasa : ");
            String rasa = myObj.nextLine();
            k2.setRasa(rasa);

            System.out.print("Bentuk Kemasan : ");
            String kemasan = myObj.nextLine();
            k2.setKemasan(kemasan);

            System.out.print("Warna Kemasan : ");
            String kemasan = myObj.nextLine();
            k2.setWarna(warna);

            System.out.println('\n');
            this.jenisBrownies.add(k2);
        }

        System.out.println("\n");
        myObj.close();
        return this.jenisBrownies;

    }

    public void ShowListBrownies(){

        for (String x : MyBrowniesi) {
            System.out.println("Brownies yang sudah ada yaitu : "+ x);
        }

    }

}
