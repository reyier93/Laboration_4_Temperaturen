# Laboration_4_Temperaturen
Labb 4

package laboration4;

import java.util.Arrays;
import java.util.Random;

public class Laboration4a {

    public static void main(String[] args) {
        Random randomObj = new Random();
        int[] temp = new int [31];
        
        for (int i = 0; i < temp.length; i++) {
            temp[i] = randomObj.nextInt(15)+ 10;
        }//end for
        System.out.println(Arrays.toString(temp));
        
        int hogstaTemp = temp[0];
        for (int grader : temp) {
            if (grader > hogstaTemp) {
                hogstaTemp = grader;
            }//end if-sats
        }//end for
        System.out.println("Den högsta temperaturen i maj månad var: " + hogstaTemp + "°C");
        
        int lagstaTemp = temp[0];
        for (int grader : temp) {
            if (grader < lagstaTemp) {
                lagstaTemp = grader;
            }//end if-sats
        }//end for
        System.out.println("Den lägsta temperaturen i maj månad var: " + lagstaTemp + "°C");
        
        int medelTemp = 0;
        for (int i = 0; i < temp.length; i++) {
            medelTemp = medelTemp + temp[i];
        }//end for
        int medel = medelTemp / temp.length;
        System.out.println("Medeltemperaturen under maj månad var: " + medel + "°C");
        
        int sum = 0;
        int medianTemp = (temp.length / 2) -1;
        for (int i = 0; i < temp.length; i++) {
            sum += Math.pow((temp[i] - medelTemp), 2);
        }//end for
        System.out.println("Mediantemperaturen för maj månad var: " + medianTemp + "°C");
        
        
        
    }//end main
    
}//end class
