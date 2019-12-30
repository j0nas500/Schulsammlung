---
date: 2018-11-21
title: AutoSimulation
#video_id: _iH8f5alzWA
#description: Have non-technical people update Jekyll sites
categories:
  - Informatik
#resources:
#  - name: Source code
#    link: https://github.com/CloudCannon/creative-jekyll-theme/
#  - name: CloudCannon
#    link: https://cloudcannon.com
description: AutoSimulation geschrieben in Java
type: Document #(Video)
#set: getting-started
#set_order: 1
---



~~~ java
import java.text.DecimalFormat;
import java.util.Scanner;

public class driver {



    public static void main(String[] args) {

        DecimalFormat df = new DecimalFormat("####0.00");

        int Fahrzeug;
        int TankenFahren;
        double Strecke;
        double Tankfüllung;
        double Tankfüllungstrecke;
        int minTank, maxTank;
        double Verbrauch;
        double newTankfüllung;
        int Schleifeimmertrue;
        double kmstand;

        minTank = 5; // Liter
        maxTank = 60; // Liter
        Verbrauch = 10; // L/100km
        newTankfüllung = 0;
        Tankfüllungstrecke = 0;
        TankenFahren = 0;
        Schleifeimmertrue = 3;
        kmstand = 0;





       /* Scanner Fahrzeugchooser = new Scanner(System.in);

        System.out.println("Mit welchem Fahrzeug möchtest du fahren?\nZur Auswahl stehen Bughattie (1), Ford (2)\n");
        Fahrzeug = Fahrzeugchooser.nextInt();

        switch (Fahrzeug){

            case 1:
                System.out.println("Ok Du sitzt nun in einem Bughtatti");
                break;
            case 2:
                System.out.println("Ok Du sitzt nun in einem Ford");
                break;

        } */
        Scanner Verbrauchchooser = new Scanner(System.in);
        System.out.println("Wie groß ist dein Verbrauch? (L/100km)");
        Verbrauch = Verbrauchchooser.nextInt();

        if (Verbrauch<1) {
            System.out.println("Dein Verbrauch muss mind. 1 sein");
            System.exit(0);
        }
        else
            System.out.println("Dein Verbrauch beträgt: " + df.format(Verbrauch) + "L/100km");


        Scanner TankfüllungStartchooser = new Scanner(System.in);


        System.out.println("Wie voll ist dein Tank? (in L)");
        Tankfüllung = TankfüllungStartchooser.nextInt();


        if (Tankfüllung < minTank) {
            System.out.println("Die Tankstelle erlaubt es dir nur mind. 5L zu tanken");
            System.exit(0);
        }
        if (Tankfüllung > maxTank) {
            System.out.println("Dein Tank erlaubt es dir nur " + maxTank + "L zu tanken");
            System.exit(0);
        }
        if (Tankfüllung > minTank && Tankfüllung <= maxTank) {
            Tankfüllungstrecke = Tankfüllung / Verbrauch * 100 -20; //Schutz vor kompletten Entleerung
            System.out.println("Dein Tank ist mit " + df.format(Tankfüllung) + "L befüllt. Du kannst damit bis zu " + df.format(Tankfüllungstrecke) + "(+20)KM fahren.\n");
        }




        loop: while (Schleifeimmertrue==3) {
            Scanner TankenFahrenchooser = new Scanner(System.in);
            System.out.println("Was willst du nun machen?");
            System.out.println("(1) Fahrzeug auftanken");
            System.out.println("(2) Mit dem Fahrzeug fahren");
            System.out.println("(3) Programm beenden");
            TankenFahren = TankenFahrenchooser.nextInt();

            switch (TankenFahren) {

                case 1:
                    System.out.println("Tanken");
                    Scanner Tankfüllungchooser = new Scanner(System.in);


                    System.out.println("Wie voll ist dein Tank? (in L)");
                    Tankfüllung = Tankfüllungchooser.nextInt();


                    if (Tankfüllung < minTank) {
                        System.out.println("Die Tankstelle erlaubt es dir nur mind. 5L zu tanken");
                        //System.exit(0);
                        continue loop;
                    }
                    if (Tankfüllung > maxTank) {
                        System.out.println("Dein Tank erlaubt es dir nur " + maxTank + "L zu tanken");
                        //System.exit(0);
                        continue loop;
                    }
                    if (Tankfüllung > minTank && Tankfüllung <= maxTank) {
                        Tankfüllungstrecke = Tankfüllung / Verbrauch * 100 -20; //Schutz vor kompletten Entleerung
                        System.out.println("Dein Tank ist mit " + df.format(Tankfüllung) + "L befüllt. Du kannst damit bis zu " + df.format(Tankfüllungstrecke) + "(+20)KM fahren.\n");
                    }
                    continue loop;

                case 2:
                    System.out.println("Fahren");
                    Scanner Streckechooser = new Scanner(System.in);

                    System.out.println("Wie weit möchtest du mit deinem Fahrzeug fahren? (in KM) (Max: " + df.format(Tankfüllungstrecke) + "KM)" + Tankfüllung);
                    Strecke = Streckechooser.nextInt();
                    kmstand = Strecke + kmstand;

                    if (Strecke > Tankfüllungstrecke) {
                        System.out.println("Unmöglich. Du wirst nie an dein Ziel ankommen");
                        continue loop;
                    } else {
                        do {
                            Tankfüllung = Tankfüllung - (Verbrauch / 100);
                            Tankfüllungstrecke = Tankfüllung / 0.1;
                            Strecke--;
                            System.out.println(Strecke + "Du musst nur noch " + Strecke + "KM fahren. Dein Tank beträgt nun nur noch " + df.format(Tankfüllung) + "L." + " Du kannst nur noch " + df.format(Tankfüllungstrecke) + "KM weit fahren.");
                        } while (Strecke > 0);
                        System.out.println("\n\nDu bist an dein Ziel angekommen. Du hast nur noch " + df.format(Tankfüllung) + "L.");
                        System.out.println("Dein Kilometerstand: " + df.format(kmstand) + "KM");
                        continue loop;
                    }
                case 3:
                    System.out.println("Programm beendet.");
                    break loop;
            }







       /*newTankfüllung=Strecke/Verbrauch*Strecke;
       System.out.println("Dein Tank beträgt nun nur noch "+ newTankfüllung + "L.");*/


        }

    }

}
~~~
