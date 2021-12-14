package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
            Scanner scan = new Scanner(System.in);
            Scanner scan1 = new Scanner(System.in);
            int num;
            SimCard[] simCards = new SimCard[2];
            simCards[0] = new SimCard("O!", 50, 1);
            simCards[1] = new SimCard("Megacom", 10, 2);
            MobilePhone mobilePhone = new MobilePhone("Redmi Note 4X", "Black", simCards);
        //System.out.println(mobilePhone);
            do {
                System.out.println("Нажмите на одну из цифр, чтобы выполнить действия:\n" +
                        "0 - выключить телефон. \n" +
                        "1 - позвонить. \n" +
                        "2 - отправить сообщение. \n" +
                        //Добавить ввести номер
                        "3 - использовать интернет. \n" +
                        "4 - получить информацию о телефоне. \n");
                num = scan.nextInt();
                switch(num) {
                    case 0:
                        System.out.println("Отключение телефона!");
                        break;
                    case 1:
                        System.out.println("Введите номер телефона: (пример: 0558501930):");
                        String number = scan1.nextLine();
                        simCards[0].setPrices(number);
                        simCards[1].setPrices(number);
                        if (simCards[0].getCorrectNumber() && simCards[0].getCallPrice() <
                                simCards[1].getCallPrice())
                                simCards[0].callTo();
                        else if(simCards[1].getCorrectNumber()) simCards[1].callTo();
                        else System.out.println("Вы ввели номер неправильно или " +
                                    "вы ввели неправильный код оператора!");
                        break;
                    case 2:
                        System.out.println("Введите номер телефона: (пример: 0558501930):");
                        String number1 = scan1.nextLine();
                        simCards[0].setPrices(number1);
                        simCards[1].setPrices(number1);
                        if (simCards[0].getCorrectNumber() && simCards[0].getSmsPrice() <
                                simCards[1].getSmsPrice())
                            simCards[0].messageTo();
                        else if(simCards[1].getCorrectNumber()) simCards[1].messageTo();
                        else System.out.println("Вы ввели номер неправильно или " +
                                    "вы ввели неправильный код оператора!");
                        break;
                    case 3:
                        System.out.println("Какую сим-карту использовать для интернета (1 или 2)?");
                        int j = -1 + scan1.nextInt();
                        simCards[j].internetUse();
                        break;
                    case 4:
                        System.out.println(mobilePhone);
                        break;
                    default:
                        System.out.println("Вы ввели неправильную команду");
                        break;
                }
            } while(num != 0);
        }
}
