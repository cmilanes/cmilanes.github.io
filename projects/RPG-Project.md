---
layout: project
type: project
image: img/RPG-Image.jpg
title: "Text-Based RPG"
date: 2019
published: true
labels:
  - Java
  - Object Oriented Programming
summary: "The text based RPG project was developed for AP Computer Science in order to develop our knowledge in Java and object oriented programming."
---

<img class="img-fluid" src="../img/RPG-Image.jpg">
 
For AP computer science in high school, one of the final project we were tasked with designing was a text-based RPG to apply what we learned about object oriented programming into a project. The project involved the creation of various parent and child classes for the different types of characters that the player of the game could select. This went hand in hand with creating mutators and accessors for the various classes and using them to program how they would interact in the main gameplay loop. In addition to the player classes, the ability to create and read save data was a feature for the game. This was done using some simple file I/O methods in Java in order read a file, parse the data, and use the data in the game.  

Shown below is a code snippet for the main character creation class:
```
public class Character extends Mappable{
    public static final int STARTING_HP = 40;
    private int strength;
    private int health;
    private int defence;
    private int agility;
    private int range;
    private String name;
    private int xp;

    public Character(String name, int str, int def, int exp, int r, int c, int range, int agil){
        super(r,c);
        name = name;
        strength = str;
        defence = def;
        health = STARTING_HP;
        xp = exp;
        this.range = range;
        this.agility = agil;
    }

    public Character(String name, int r, int c){
        super(r,c);
        strength = (int)(Math.random() * 30.0);
        defence =  30 - strength;
        health = STARTING_HP;
        xp = 10;
        this.name = name;
        System.out.println(name + "\n" + "Str: " + strength + "\n" + "Def: " + defence + "\n" + "Hp: " + health + "\n" + "________________________");  
    }

    public Character(int r, int c){
        super(r,c);
    }
```
