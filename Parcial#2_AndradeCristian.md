/*
UNIVERSIDAD TECNOLOGICA DE PANAMA
FACULTAD DE INGENIERIA DE SISTEMAS
LICENCIATURA EN DESARROLLO DE SOFTWARE
PARCIAL#2
DESARROLLO DE SOFTWARE III
2022

INTEGRANTES:
Cristian Andrade 3-749-573
Prof. Fellicita De Krol

*/

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.FileReader;
import java.io.File; 

public class Main { 
  public static void main(String[] args) {
    File myObj = new File("numero.csv");
    if (myObj.exists()) {
      System.out.println("Nombre del archivo: " + myObj.getName());
      System.out.println("Ruta del archivo: " + myObj.getAbsolutePath());
      System.out.println("Writeable: " + myObj.canWrite());
      System.out.println("Readable " + myObj.canRead());
      System.out.println("tamano del archivo en byte " + myObj.length());
    } else {
      System.out.println("The file does not exist.");
    }
        File file = new File(myObj.getAbsolutePath());
        File rename = new File("/home/numero2.txt");
        boolean flag = file.renameTo(rename);
        if (flag == true) {
            System.out.println("El nombre del archivo a sido cambiado efectivamente");
        } else {
            System.out.println("La operacion a fallado");
        }
        System.out.println("Nombre del archivo: " + rename.getName());
  }
}
