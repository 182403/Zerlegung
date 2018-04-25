# Zerlegung
Zerlegung von Zahlen
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package zerlegung.von.zahlen;

/**
 *
 * @author ja-182403
 */
import java.util.Scanner;

public class ZerlegungVonZahlen {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Scanner ts = new Scanner(System.in);
        System.out.println("Zahl angeben: ");
        int number = ts.nextInt();
        String tmpString = "" + number;
        int[] numberArray = new int[tmpString.length()];
        for (int i = 0; i < tmpString.length(); i++) {
            numberArray[i] = Integer.parseInt(tmpString.substring(i, i + 1));
        }

        float dualzahl = chalculatedual(number, numberArray);
        
        System.out.println(number);
        for (int i = 0; i < numberArray.length; i = i + 1) {
            System.out.print(numberArray[i] + "\t");
        }
        System.out.println("");
        System.out.print(dualzahl);
    }

    static float chalculatedual(int number, int[] numberArray) {
        
        int Rest = 0;
        int[] GRest = new int[16];
        int GanzZahl = (int)number;
        while (number != 0){
            Rest = GanzZahl%2;
            GanzZahl = GanzZahl/2;
            
        } 
        return Rest;

    }

}
