# Jabberwock
printing test

import java.awt.Graphics;
public class JabberwockApplet extends java.applet.Applet {
  public void paint(Graphics g) {
    Jabberwock j = new Jabberwock();
    j.color = "Orange";
    j.sex = "male";
    j.hungry = true;
    g.drawString("calling showAtts ...", 5, 50);
    j.showAtts(g, 70);
    g.drawString("Feeding the Jabberwock ...", 5, 110);
    j.showAtts(g, 130);
    g.drawString("calling showAtts ...", 5, 150);
    j.showAtts(g, 170);
    g.drawString("Feeding the Jabberwock ...", 5, 210);
    j.showAtts(g, 230);
  }
}

class Jabberwock {
  String color;
  String sex;
  boolean hungry;

  void feedJabberwock(Graphics g, int y) {
    if (hungry == true){
      g.drawString("Yam yam", 25, y);
    hungry = false;
  }else
      g.drawString("No thanks", 25 ,y);
  }
  void showAtts(Graphics g, int y) {
    g.drawString("this is a" + sex + color + "jabberwock.", 25, y);
    if (hungry == true)
      g.drawString("the jabberwock is hungry.", 25 ,y+20);
    else
      g.drawString("the jabberwock is full.", 25 ,y+20);
    }
  }


