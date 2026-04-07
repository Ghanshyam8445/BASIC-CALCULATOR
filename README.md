# BASIC-CALCULATOR
import java.awt.*;
import java.awt.event.*;
class q2 implements ActionListener
{
    Frame f;
    Button b1,b2,b3,b4,b5,b6,b7,b8,b9,b10,b11,b12,b13,b14,b15,b16,b17,b18;
    TextField t1;
    String sign;
    double a,b,c; 
    q2()
    {
        f=new Frame("Calculator");
        b1=new Button("9");
        b2=new Button("8");
        b3=new Button("7");
        b4=new Button("/");
        b5=new Button("6");
        b6=new Button("5");
        b7=new Button("4");
        b8=new Button("*");
        b9=new Button("3");
        b10=new Button("2");
        b11=new Button("1");
        b12=new Button("-");
        b13=new Button("00");
        b14=new Button("0");
        b15=new Button("=");
        b16=new Button("+");
        b17=new Button("Back Space");
        b18=new Button("clear");
        t1=new TextField();
        t1.setBounds(20,40,350,30);
        b1.setBounds(20,90,70,30);
        b2.setBounds(100,90,70,30);
        b3.setBounds(180,90,70,30);
        b4.setBounds(260,90,70,30);
        b5.setBounds(20,130,70,30);
        b6.setBounds(100,130,70,30);
        b7.setBounds(180,130,70,30);
        b8.setBounds(260,130,70,30);
        b9.setBounds(20,170,70,30);
        b10.setBounds(100,170,70,30);
        b11.setBounds(180,170,70,30);
        b12.setBounds(260,170,70,30);
        b13.setBounds(20,210,70,30);
        b14.setBounds(100,210,70,30);
        b15.setBounds(180,210,70,30);
        b16.setBounds(260,210,70,70);
        b17.setBounds(20,250,150,30);
        b18.setBounds(180,250,70,30);
        f.add(b1);
        f.add(b2);
        f.add(b3);
        f.add(b4);
        f.add(b5);
        f.add(b6);
        f.add(b7);
        f.add(b8);
        f.add(b9);
        f.add(b10);
        f.add(b11);
        f.add(b12);
        f.add(b13);
        f.add(b14);
        f.add(b15);
        f.add(b16);
        f.add(b17);
        f.add(b18);
        f.add(t1);
        b1.addActionListener(this);
        b2.addActionListener(this);
        b3.addActionListener(this);
        b4.addActionListener(this);
        b5.addActionListener(this);
        b6.addActionListener(this);
        b7.addActionListener(this);
        b8.addActionListener(this);
        b9.addActionListener(this);
        b10.addActionListener(this);
        b11.addActionListener(this);
        b12.addActionListener(this);
        b13.addActionListener(this);
        b14.addActionListener(this);
        b15.addActionListener(this);
        b16.addActionListener(this);
        b17.addActionListener(this);
        b18.addActionListener(this);
        f.setSize(400,300);
        f.setLayout(null);
        f.setVisible(true);
    }
    public void actionPerformed(ActionEvent ae)
    {
        if (ae.getSource()==b1)
        {
            t1.setText(t1.getText()+"9");
        }
        else if (ae.getSource()==b2)
        {
            t1.setText(t1.getText()+"8");
        }
        else if (ae.getSource()==b3)
        {
            t1.setText(t1.getText()+"7");
        }
        else if (ae.getSource()==b4)
        {
            t1.setText(t1.getText()+"/");
            sign="/";
        }
        else if (ae.getSource()==b5)
        {
            t1.setText(t1.getText()+"6");
        }
        else if (ae.getSource()==b6)
        {
          t1.setText(t1.getText()+"5");
        }
        else if (ae.getSource()==b7)
        {
            t1.setText(t1.getText()+"4");
        }
        else if (ae.getSource()==b8)
        {
            t1.setText(t1.getText()+"*");
            sign="*";
        }
        else if (ae.getSource()==b9)
        {
            t1.setText(t1.getText()+"3");
        }
        else if (ae.getSource()==b10)
        {
          t1.setText(t1.getText()+"2");
        }
        else if (ae.getSource()==b11)
        {
           t1.setText(t1.getText()+"1");
        }
        else if (ae.getSource()==b12)
        {
             t1.setText(t1.getText()+"-");
            sign="-";
        }
        else if (ae.getSource()==b13)
        {
            t1.setText(t1.getText()+"00");
        }
        else if (ae.getSource()==b14)
        {
           t1.setText(t1.getText()+"0");
        }        
        else if (ae.getSource()==b16)
        {
             t1.setText(t1.getText()+"+"); 
            sign="+";
        }
        else if (ae.getSource()==b18)
        {
             t1.setText("");
        }
        else if(ae.getSource()==b17)
        {
            String t=t1.getText();
            t=t.substring(0, t.length() - 1);
            t1.setText(t);
        }
        else if (ae.getSource()==b15)
        {
        a=Double.parseDouble(t1.getText().substring(0,t1.getText().indexOf(sign)));
        b=Double.parseDouble(t1.getText().substring(t1.getText().indexOf(sign)+1));
          if(sign.equals("+"))
          {
            c=a+b;
          }
          else if(sign.equals("-"))
          {
            c=a-b;
          }
          else if(sign.equals("*"))
          {
            c=a*b;
          }
          else if(sign.equals("/"))
          {
            c=a/b;
          }
          t1.setText(t1.getText()+"="+String.valueOf(c));
        }
    }
    public static void main(String[] args)
    {
        q2 q=new q2();  
    }
}
