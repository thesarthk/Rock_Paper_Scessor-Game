# Rock_Paper_Scessor-Game
//By using Java we have maked a ROCK PAPER SCESSOR Game -->
import java.util.Random;
import java.util.Scanner;
public class RockPS {
    public static void main(String[] args){


        Random ss= new Random();
        int aa = ss.nextInt(3);

        Scanner GiveNo =new Scanner(System.in);
        Scanner Name =new Scanner(System.in);
        String Computer=" ";
        String User=" ";
        Byte play;

        if(aa==0){
            Computer="rock";
        }
        else if(aa==1){
            Computer="Scissor";
        }
        else if(aa==2){
            Computer="Paper";
        }

//        System.out.print(Computer);

        System.out.print("Hey User Please Type Your Name:- ");
         String UserName =GiveNo.nextLine();

      do {
          System.out.println("Press---->\n\t 1=Rock \n\t 2=Scissor \n\t 3=Paper\n");
//         System.out.print("Random:-"+aa);
        System.out.print(" \t\t\t*******lets Play The Game*******\n\tChoose your Option Number:-");
        Byte TakeANumber= GiveNo.nextByte();

        if(TakeANumber>0 && TakeANumber<3){

            if (TakeANumber == 1) {
                User = "rock";
            } else if (TakeANumber == 2) {
                User = "Scissor";
            } else if (TakeANumber == 3) {
                User = "Paper";
            }

            System.out.println("\t\t*********************");
            System.out.println("Uponent's Choise:-" + Computer + "\t\t" + UserName + " Your's Choise:-" + User);
            System.out.println("\t\t*********************");

            if (aa == TakeANumber) {
                System.out.println("|| Match is Tie ||" + "\n\n");
            } else if (aa == 0 && TakeANumber == 2) {
                System.out.println("Oops....U Loose This Game...Better Luck Next Time");
            } else if (aa == 0 && TakeANumber == 3) {
                System.out.println("\nHuryeee...\n\t|| U Won The Match ||");
            } else if (aa == 1 && TakeANumber == 1) {
                System.out.println("\nHuryeee...\n\t|| U Won The Match ||");
            } else if (aa == 1 && TakeANumber == 3) {
                System.out.println("Oops....U Loose This Game...Better Luck Next Time");
            } else if (aa == 2 && TakeANumber == 1) {
                System.out.println("Oops....U Loose This Game...Better Luck Next Time");
            } else if (aa == 2 && TakeANumber == 2) {
                System.out.println("\n" + "Huryeee...\n" + "\t|| U Won The Match ||");
            }
        }
        else {
            System.out.println("Hey Player U Enter a WRONG NUMBER Please Select a Right Choise");
        }
        System.out.println("Do You wanna playyyy Again:- ");
          System.out.println("If Yes Choose:-1"+"\n"+ "If No Choose :-0");
          System.out.print("Enter Your Choice:-");
        play= GiveNo.nextByte();

      }while(play==1);
      }
}
