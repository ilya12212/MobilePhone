package com.company;

import java.util.Scanner;

public class SimCard {
    private String name;
    private int simCardNumber;
    private double balance;
    String numberCallTo;
    private double callPrice;
    private double smsPrice;
    private double internetPrice;
    public boolean correctNumber;

    public SimCard(String name, double balance, int simCardNumber) {
        this.name = name;
        this.balance = balance;
        this.simCardNumber = simCardNumber;
        setInternetPrice();
    }

    public SimCard() {

    }

    public void setCorrectNumber(boolean correctNumber) {
        this.correctNumber = correctNumber;
    }

    public void setName(String name) {
        this.name = name;
    }

    public void setSimCardNumber(int simCardNumber) {
        this.simCardNumber = simCardNumber;
    }

    private void setBalance(double balance) {
        this.balance = balance;
    }

    public void setCallPrice(double callPrice) {
        this.callPrice = callPrice;
    }

    public void setSmsPrice(double smsPrice) {
        this.smsPrice = smsPrice;
    }

    public void setInternetPrice() {
        switch (name) {
            case "O!":
                this.internetPrice = 30;
                break;
            case "Beeline":
                this.internetPrice = 30;
                break;
            case "Megacom":
                this.internetPrice = 40;
                break;
        }
    }

    public void setNumberCallTo(String numberCallTo) {
        this.numberCallTo = numberCallTo;
    }

    public String getName() {
        return name;
    }

    public boolean getCorrectNumber() {
        return correctNumber;
    }

    public int getSimCardNumber() {
        return simCardNumber;
    }

    public double getBalance() {
        return balance;
    }

    public double getCallPrice() {
        return callPrice;
    }

    public double getSmsPrice() {
        return smsPrice;
    }

    public double getInternetPrice() {
        return internetPrice;
    }

    public String getNumberCallTo() {
        return numberCallTo;
    }

    public void callTo() {

        System.out.println("Вы звоните на номер " + getNumberCallTo());
        System.out.println("Стоимость звонка: " + getCallPrice());
        if (balance < getCallPrice()) {
            System.out.println("Недостаточно средств на балансе для использования интернета!");
        } else {
            balance -= getCallPrice();
            System.out.println("Вызов завершён.");
        }
        System.out.println("Ваш баланс: " + getBalance());
    }

    public void messageTo() {
        Scanner scan = new Scanner(System.in);
        System.out.println("Вы пишете на номер " + numberCallTo);
        System.out.println("Стоимость смс: " + getSmsPrice());
        if (balance < getSmsPrice()) {
            System.out.println("Недостаточно средств на балансе для использования интернета!");
        } else {
            balance -= getSmsPrice();
            System.out.print("Введите сообщение: ");
            scan.nextLine();
            System.out.println("Ваше сообщение отправлено!\n");
        }
        System.out.println("Ваш баланс: " + getBalance());
    }

    public void internetUse() {
        System.out.println("Вы включили интернет.");
        System.out.println("Стоимость 1 ГБ: " + getInternetPrice());
        if (balance < getInternetPrice()) {
            System.out.println("Недостаточно средств на балансе для использования интернета!");
        } else {
            balance -= getInternetPrice();
            System.out.println("Вы воспользовались интернетом!");
        }
        System.out.println("Ваш баланс: " + getBalance());
    }

    public void setPrices(String num) {
        byte[] nums = new byte[10];
        if (num.length() == 10) {
                nums = num.getBytes();
                for (int i = 0; i < nums.length; i++) {
                    nums[i] -= 48;
                }
        if (nums[0] == 0 && nums[1] == 5 && nums[2] == 5 &&
                nums[3] >=0 && nums[3] <= 9) {
            setNumberCallTo(num);
            setCorrectNumber(true);
            switch (name) {
                case "O!":
                    setCallPrice(0.95);
                    setSmsPrice(2);
                    break;
                case "Beeline":
                    setCallPrice(1);
                    setSmsPrice(1.2);
                    break;
                case "Megacom":
                    setCallPrice(0);
                    setSmsPrice(0);
                    break;
            }
        } else if (nums[0] == 0 && nums[1] == 5 && nums[2] == 0 &&
                nums[3] >= 0 && nums[3] <= 9) {
            setNumberCallTo(num);
            setCorrectNumber(true);
            switch (name) {
                case "O!":
                    setCallPrice(0);
                    setSmsPrice(0);
                    break;
                case "Beeline":
                    setCallPrice(1);
                    setSmsPrice(1.2);
                    break;
                case "Megacom":
                    setCallPrice(1.05);
                    setSmsPrice(1.7);
                    break;
            }
        } else if (nums[0] == 0 && nums[1] == 7 && nums[2] == 7 &&
                nums[3] >=0 && nums[3] <= 9) {
            setNumberCallTo(num);
            setCorrectNumber(true);
            switch (name) {
                case "O!":
                    setCallPrice(0.95);
                    setSmsPrice(2);
                    break;
                case "Beeline":
                    setCallPrice(0);
                    setSmsPrice(0);
                    break;
                case "Megacom":
                    setCallPrice(1.05);
                    setSmsPrice(1.7);
                    break;
            }
        } else setCorrectNumber(false);
        } else setCorrectNumber(false);
    }

    @Override
    public String toString() {
        String message = "Информация о " + simCardNumber + " сим-карте:" + "\n" +
                "Название оператора: " + name + "\n" +
                "Баланс: " + balance + "\n";
        return message;
    }
}
