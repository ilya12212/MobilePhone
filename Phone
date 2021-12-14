package com.company;

public class MobilePhone {
    String model;
    String color;
    SimCard[] simCards = new SimCard[2];
    byte needSimCard = 0;

    public MobilePhone(String model, String color, SimCard[] simCards) {
        this.model = model;
        this.color = color;
        this.simCards = simCards;
    }

    public MobilePhone() {

    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setColor(String color) {
        this.color = color;
    }

    public void setSimCards(SimCard[] simCards) {
        this.simCards = simCards;
    }

    public String getModel() {
        return model;
    }

    public String getColor() {
        return color;
    }

    public SimCard getSimCard(int simCardNumber) {
        return simCards[simCardNumber];
    }

    @Override
    public String toString() {
        String message = "Информация о телефоне: " + "\n" +
                "Марка телефона: " + getModel() + "\n" +
                "Цвет телефона: " + getColor() + "\n" +
                getSimCard(0) +
                getSimCard(1);
        return message;
    }
}
