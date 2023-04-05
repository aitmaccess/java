1.

import java.util.Scanner;

import java.lang.*;

public class OOP1 {

public static void main(String[] args) {

int a,b,c,d;

double x1,x2;

Scanner sc=new Scanner(System.in);

System.out.println("entre the values of a,b,c");

a=sc.nextInt();

b=sc.nextInt();

c=sc.nextInt();

d=(b*b-4*a*c);

if(d==0)

{

x1=x2=-b/(2*a);

System.out.println("the roots are"+" and "+x2);

}

else if(d>0)

{

x1=-b+Math.sqrt(d)/(2*a);

x2=-b-Math.sqrt(d)/(2*a);

System.out.println("the roots are"+x1+" and "+x2);

}

else

{

System.out.println("the roots are imaginary");

}

} }


2.

import java.util.Scanner;

class student {

String name;

String usn;

String branch;

long phone;

void display()

{

System.out.println(" name is: "+name);

System.out.println(" usn is: "+usn);

System.out.println(" branch is: "+branch);

System.out.println(" phone is: "+phone);

}

}

public class OOP2 {

public static void main(String[] args) {

// TODO Auto-generated method stub

int n;

student s[]=new student[100];

Scanner sc=new Scanner(System.in);

System.out.println("enter the no of students ");

n=sc.nextInt();

for(int i=1;i<=n;i++)

{

s[i]=new student();

System.out.println("enter the name ");

s[i].name=sc.next();

System.out.println("enter the usn ");

s[i].usn=sc.next();

System.out.println("enter the branch ");

s[i].branch=sc.next();

System.out.println("enter the phone ");

s[i].phone=sc.nextLong();

}

System.out.println("student details ");

for(int i=1;i<=n;i++)

{

System.out.println("details of student: "+i);

s[i].display();

}

}

}

3a.

import java.util.Scanner;

public class OOP3a {

public static void main(String[] args) {

// TODO Auto-generated method stub

int n,m,flag=0;

Scanner sc=new Scanner(System.in);

System.out.println("enter the number ");

n=sc.nextInt();

m=n/2;

if(n==0||n==1){

System.out.println(n+" is not prime number");

}else{

for(int i=2;i<=m;i++){

if(n%i==0){

System.out.println(n+" is not prime number");

flag=1;

break;

}

8 }

if(flag==0) { System.out.println(n+" is prime number"); }

}//end of else

}

}

3b.

import java.util.Scanner;

public class OOP3b {

public static void main(String[] args) {

// TODO Auto-generated method stub

// TODO Auto-generated method stub

char oper;

double op1,op2,res;

Scanner sc=new Scanner(System.in);

System.out.println("enter the operator: +,-,*,/,%");

oper=sc.next().charAt(0);

System.out.println("enter the operand1 ");

op1=sc.nextDouble();

System.out.println("enter the operand2 ");

op2=sc.nextInt();

switch(oper)

{

case '+':res=op1+op2;

System.out.println("The sum of two numbers is: "+res); break;

case '-':res=op1-op2;

System.out.println("The difference of two numbers is: "+res);
break;

case '*':res=op1*op2;

System.out.println("The product of two numbers is: "+res); break;

case '/':res=op1/op2;

System.out.println("The division of two numbers is: "+res); break;

case '%':res=op1%op2;

System.out.println("The modulus of two numbers is: "+res); break;

default:System.out.println("wrong operator ");

break;

}

}

}


4.

import java.util.Scanner;

class staff_college

{

String staffid;

String name;

String phone;

double salary;

}

class teaching extends staff_college

{

String domain;

String publications;

void display(String dom,String pub)

{

domain=dom;

publications=pub;

System.out.println(" the Teacher details ");

System.out.println("staffid: "+staffid);

System.out.println("name: "+name);

System.out.println("phone: "+phone);

System.out.println("salary: "+salary);

System.out.println("domain: "+domain);

System.out.println("publications: "+publications);

}

}

class technical extends staff_college

{

String skills;

void display(String skills)

{

System.out.println(" the Technical staff details ");

System.out.println("staffid: "+staffid);

System.out.println("name: "+name);

System.out.println("phone: "+phone);

System.out.println("salary: "+salary);

System.out.println("skills: "+skills);

}

}

class contract extends staff_college

{

String period;

void display(String per)

{

System.out.println(" the Contract staff details ");

System.out.println("staffid: "+staffid);

System.out.println("name: "+name);

System.out.println("phone: "+phone);

System.out.println("salary: "+salary);

System.out.println("period: "+period);

}

}
public class OOP4 {

public static void main(String[] args) {

String dom,pub,skills,per;

staff_college s=new staff_college();

teaching t1=new teaching();

technical t2=new technical();

contract t3=new contract();

Scanner sc=new Scanner(System.in);

System.out.println("enter the Teacher details ");

System.out.println("enter staff id of the staff: ");

t1.staffid=sc.next();

System.out.println("enter name of the staff: ");

t1.name=sc.next();

System.out.println("enter phone of the staff: ");

t1.phone=sc.next();

System.out.println("enter salary of the staff: ");

t1.salary=sc.nextDouble();

System.out.println("enter domain of the staff: ");

dom=sc.next();

System.out.println("enter publications of the staff: ");

pub=sc.next();

System.out.println("enter the Technical staff details ");

System.out.println("enter staff id of the staff: ");

t2.staffid=sc.next();

System.out.println("enter name of the staff: ");

t2.name=sc.next();

System.out.println("enter phone of the staff: ");

t2.phone=sc.next();

System.out.println("enter salary of the staff: ");

t2.salary=sc.nextDouble();

System.out.println("enter skills of the staff: ");

skills=sc.next();

System.out.println("enter the contractor details ");

System.out.println("enter staff id of the staff: ");

t3.staffid=sc.next();

System.out.println("enter name of the staff: ");

t3.name=sc.next();

System.out.println("enter phone of the staff: ");

t3.phone=sc.next();

System.out.println("enter salary of the staff: ");

t3.salary=sc.nextDouble();

System.out.println("enter period : ");

per=sc.next();

t1.display(dom,pub);

t2.display(skills);

t3.display(per);

}

}


5.

class constructor_area

{

int length,breadth;

void area()

{

System.out.println("This is Method overloading");

}

void area(int s)

{

int a;

a=s*s;

System.out.println("the side of a square is"+" "+s);

System.out.println("The area of a square under method overloading is:"+a);

}

void area(int l,int b)

{

int a;

a=l*b;

System.out.println("the length and breadth of a rectangle is"+" "+l+" "+b);

System.out.println("The area of a rectangle under method overloading is:"+a);

}

constructor_area()

{

System.out.println("This is a Constructor overloading");

}

constructor_area(int s)

{

int a;

a=s*s;

System.out.println("the side of a square is"+" "+s);

System.out.println("The area of a square under constructor overloading is:"+a);

}

constructor_area(int l,int b)

{

int a;

length=l;

breadth=b;

System.out.println("the length and breadth of a rectangle is"+" "+length+" "+breadth);

a=length*breadth;

System.out.println("The area of rectangle under constructor overloading is: "+a);

}

}

public class OOP5 {

public static void main(String[] args) {

// TODO Auto-generated method stub

constructor_area c=new constructor_area();

constructor_area c1=new constructor_area(2,3);

constructor_area c2=new constructor_area(3);

c.area();

c.area(4);

c.area(4,5);

}

}

6. 

import java.util.*;

import java.text.DecimalFormat;

import java.lang.*;

public class OOP6 {

public static void main(String[] args) {

// TODO Auto-generated method stub

int ch;

double rupee,dollar,code,euro,yen,kilometer,meter,miles,hours,min,sec;

DecimalFormat f = new DecimalFormat("##.###");

Scanner sc = new Scanner(System.in);

while(true)

{System.out.println("Enter your choice for conversion: \n1:currency converter \t2:Distance converter

\t3:Time converter\t 4:exit\n");

ch=sc.nextInt();

switch(ch)

{

case 1:

System.out.println("Enter amount in dollar to convert into rupee:");

dollar = sc.nextFloat();

rupee = dollar * 75;

System.out.println("Rupees : "+f.format(rupee));

System.out.println("Enter amount in Euro to convert into rupee:");

euro = sc.nextFloat();

rupee = euro * 84;

System.out.println("Rupees : "+f.format(rupee));

System.out.println("Enter amount in YEN to convert into rupee:");

yen = sc.nextFloat();

rupee = yen /0.59;

System.out.println("Rupees : "+f.format(rupee));

System.out.println("Enter amount in INR to convert to Dollar:");

rupee = sc.nextFloat();

dollar = rupee / 75;

System.out.println("Dollar : "+f.format(dollar));

System.out.println("Enter amount in INR to convert to Euro:");

rupee = sc.nextFloat();

euro = rupee/84;

System.out.println("Rupees : "+f.format(euro));

System.out.println("Enter amount in INR to convert to Yen:");

rupee = sc.nextFloat();

yen = 0.59*rupee;

System.out.println("Rupees : "+f.format(yen));

break;

case 2:

System.out.println("Enter number in meter to convert into kilometer:"); meter

= sc.nextFloat();

kilometer = meter * 1000;

System.out.println("kilometer : "+f.format(kilometer));

System.out.println("Enter number in miles to convert into kilometer:"); miles

= sc.nextFloat();

kilometer = miles * 1.60934;

System.out.println("kilometer : "+f.format(kilometer));

System.out.println("Enter number in kilometer to convert into meter:");

kilometer = sc.nextFloat();

meter = kilometer / 1000;

System.out.println("meter : "+f.format(meter));

System.out.println("Enter number in kilometer to convert into miles:");

kilometer = sc.nextFloat();

miles = kilometer / 1.60934;

System.out.println("Miles : "+f.format( miles));

break;

case 3:

System.out.println("Enter number in hours to convert into minutes:"); hours

= sc.nextFloat();
min = hours* 60;

System.out.println("Minutes : "+f.format(min));

System.out.println("Enter number in hours to convert into Seconds:"); hours

= sc.nextFloat();

sec = hours * 3600;

System.out.println("Seconds : "+f.format(sec));

System.out.println("Enter number in minutes to convert into hours:");

min = sc.nextFloat();

hours = min /60;

System.out.println("Hours : "+f.format(hours));

System.out.println("Enter number in seconds to convert into hours:");

sec = sc.nextFloat();

hours = sec /3600;

System.out.println("Hours : "+f.format(hours));

break;

case 4:System.out.println("exiting the program");

System.exit(0);

}

}

}

}


7.

import java.util.Scanner;

interface resume

{

public void biodata();

}

class teacher implements resume

{

String name;

String emailid;

long phone;

String address;

int age;

String qualification;

float experience;

String acheivements;

@Override

public void biodata() {

// TODO Auto-generated method stub

System.out.println("The Teacher details are:");

System.out.println("The name :"+name);

System.out.println("The emailid:"+emailid);

System.out.println("phone:"+phone);

System.out.println("address:"+address);

System.out.println("age:"+age);

System.out.println("qualification:"+qualification);

System.out.println("experience:"+experience);

System.out.println("acheivements:"+acheivements);

}

}

class student_resume implements resume

{

String name;

String emailid;

long phone;

String address;

int age;

double result;

String discipline;

@Override

public void biodata() {

// TODO Auto-generated method stub

System.out.println("The Student details are:");

System.out.println("The name :"+name);

System.out.println("The emailid:"+emailid);

System.out.println("phone:"+phone);

System.out.println("address:"+address);

System.out.println("age:"+age);

System.out.println("result:"+result);

System.out.println("discipline:"+discipline);
}

}

public class OOP7 {

public static void main(String[] args) {

// TODO Auto-generated method stub

// TODO Auto-generated method stub

String n,e,ad,q,ach,di;

int p,ag;

float re,exp;

Scanner sc = new Scanner(System.in);

teacher t=new teacher();

student_resume s=new student_resume();

System.out.println("Enter the name of the teacher:");

t.name=sc.next();

System.out.println("Enter the emailid of the teacher:");

t.emailid=sc.next();

System.out.println("Enter the phone of the teacher:");

t.phone=sc.nextLong();

System.out.println("Enter the address of the teacher:");

t.address=sc.next();

System.out.println("Enter the age of the teacher:");

t.age=sc.nextInt();

System.out.println("Enter the qualification of the teacher:");

t.qualification=sc.next();

System.out.println("Enter the experience of the teacher:");

t.experience=sc.nextFloat();

System.out.println("Enter the acheivements of the teacher:");

t.acheivements=sc.next();

t.biodata();

System.out.println("Enter the name of the student:");

s.name=sc.next();

System.out.println("Enter the emailid of the student:");

s.emailid=sc.next();

System.out.println("Enter the phone of the student:");

s.phone=sc.nextLong();

System.out.println("Enter the address of the student:");

s.address=sc.next();

System.out.println("Enter the age of the student:");

s.age=sc.nextInt();

System.out.println("Enter the result of the student:");

s.result=sc.nextDouble();

System.out.println("Enter the discipline of the student:");

s.discipline=sc.next();

s.biodata();

}

}

8.

import java.util.Random;

class random_number implements Runnable

{

public void run()

{

Random ra=new Random();

for(int i=0;i<10;i++)

{

int r = ra.nextInt(100);

System.out.println("Random number:"+r);

square s=new square(r);

s.start();

cube c=new cube(r);

c.start();

try {

Thread.sleep(1000);

} catch (InterruptedException ex) {

System.out.println(ex);

}

}

}

}

class square extends Thread

{

int x;

public square(int r) {

// TODO Auto-generated constructor stub

x=r;

}

public void run()

{

int sq;

sq=x*x;

System.out.println("Square of " + x + " = " + sq);

}

}

class cube extends Thread

{

int x;

public cube(int r) {

// TODO Auto-generated constructor stub

x=r;

}

public void run()

{
int cu;

cu=x*x*x;

System.out.println("cube of " + x + " = " + cu);

}

}

public class OOP8 {

public static void main(String[] args) {

// TODO Auto-generated method stub

random_number n=new random_number();

Thread t=new Thread(n);

t.start();

}

}

9.


import java.util.ArrayList;

import java.util.Scanner;

public class OOP9 {

public static void main(String[] args) {

// TODO Auto-generated method stub

ArrayList<String> obj = new ArrayList<String>();

Scanner sc = new Scanner(System.in);

int c,ch;

int i,j;

String str,str1;

do

{

System.out.println("STRING MANIPULATION");

System.out.println("******************************");

System.out.println(" 1. Append at end \t 2.Insert at particular index \t 3.Search

\t"); System.out.println( "4.List string that starting with letter \t");

System.out.println("Enter the choice ");

c=sc.nextInt();

switch(c)

{

case 1:

{

System.out.println("Enter the string ");

str=sc.next();

obj.add(str);

break;

}

case 2:

{

System.out.println("Enter the string ");

str=sc.next();

System.out.println("Specify the index/position to insert");

i=sc.nextInt();

obj.add(i-1,str);

System.out.println("The array list has following elements:"+obj);

break;

}

case 3:

{

System.out.println("Enter the string to search ");

str=sc.next();

j=obj.indexOf(str);

if(j==-1)

System.out.println("Element not found");

else

System.out.println("Index of:"+str+"is"+j);

break;

}

case 4:

{

System.out.println("Enter the character to List string that starts with specified

character");

str=sc.next();

for(i=0;i<(obj.size());i++)

{

str1=obj.get(i);

if(str1.startsWith(str))

{

System.out.println(str1);

}

}

break;

}

}

System.out.println("enter 0 to break and 1 to continue");

ch=sc.nextInt();

}while(ch==1);

}

}

10.

import java.util.Scanner;

public class OOP_10 {

public static void main(String[] args) {

// TODO Auto-generated method stub

int a,b,div;

Scanner sc = new Scanner(System.in);

System.out.println("Enter the value of a:");

a=sc.nextInt();

System.out.println("Enter the value of b:");

b=sc.nextInt();

try

{

div=a/b;

System.out.println("the division is"+div);

}

catch(ArithmeticException e)

{

System.out.println("the division by zero "+e.getMessage());

}

System.out.println("this is the division operation");

}

}

11.

import java.io.*;

import java.util.Scanner;

class filedemo

{

void p(String str)

{

System.out.println(str);

}

void analyze(String s)

{

File f=new File(s);

if(f.exists())

{

p(f.getName()+" is a file");

p(f.canRead()?" is readable":" is not readable");

p(f.canWrite()?" is writable":" is not writable");

p("Filesize:"+f.length()+" bytes");

p("File last modified:"+f.lastModified());

}

else

System.out.println("The file " +s+ " does not exist");

}

}

public class OOP_11 {

public static void main(String[] args) throws IOException {

// TODO Auto-generated method stub

filedemo fd=new filedemo();

Scanner sc = new Scanner(System.in);

System.out.println("Enter the file name:");

String s=sc.nextLine();

//System.out.println(s);

fd.analyze(s);

}


} 

12a.

import java.awt.*;

import java.applet.Applet;

/* <applet code="SimpleApplet" width=300 height=50> </applet>

*/ public class simpleapplet extends Applet{

public void paint(Graphics g)

{

g.drawString ("Hello world",100, 100);

}

}


12b.

import java.awt.*;

import java.awt.event.*;

public class sampleex implements ActionListener{

int c,n;

String s1,s2,s3,s4,s5;

Frame f;

Button b0, b1, b2, b3, b4, b5, b6, b7, b8, b9, badd, bsub, bmul, bdiv, beq, bclr;

Panel p;

TextField t1;

GridLayout g;

sampleex(){

f = new Frame("Calculator");

f.setLayout(new FlowLayout());

p = new Panel();

b0 = new Button("0");

b0.addActionListener(this);
b1 = new Button("1");

b1.addActionListener(this);

b2 = new Button("2");

b2.addActionListener(this);

b3 = new Button("3");

b3.addActionListener(this);

b4 = new Button("4");

b4.addActionListener(this);

b5 = new Button("5");

b5.addActionListener(this);

b6 = new Button("6");

b6.addActionListener(this);

b7 = new Button("7");

b7.addActionListener(this);

b8 = new Button("8");

b8.addActionListener(this);

b9 = new Button("9");

b9.addActionListener(this);

badd = new Button("+");

badd.addActionListener(this);

bsub = new Button("-");

bsub.addActionListener(this);

bmul = new Button("*");

bmul.addActionListener(this);

bdiv = new Button("/");

bdiv.addActionListener(this);

beq = new Button("=");

beq.addActionListener(this);

bclr = new Button("CLR");

bclr.addActionListener(this);

t1 = new TextField(20);

f.add(t1);

g = new GridLayout(4,4);

p.setLayout(g);

p.add(b0);

p.add(b1);

p.add(b2);

p.add(b3);

p.add(b4);

p.add(b5);

p.add(b6);

p.add(b7);

p.add(b8);

p.add(b9);
p.add(badd);

p.add(bsub);

p.add(bmul);

p.add(bdiv);

p.add(beq);

p.add(bclr);

f.add(p);

f.setSize(200,180);

f.setVisible(true);

f.setBackground(Color.LIGHT_GRAY);

f.addWindowListener(new WindowAdapter() {

@Override

public void windowClosing(WindowEvent e) {

System.exit(0);

}

});

}

@Override

public void actionPerformed(ActionEvent e) {

if(e.getSource()==b0){

s3 = t1.getText();

s4 = "0";

s5 = s3 + s4;

t1.setText(s5);

}

if(e.getSource()==b1){

s3 = t1.getText();

s4 = "1";

s5 = s3 + s4;

t1.setText(s5);

}

if(e.getSource()==b2){

s3 = t1.getText();

s4 = "2";

s5 = s3 + s4;

t1.setText(s5);

}

if(e.getSource()==b3){

s3 = t1.getText();

s4 = "3";

s5 = s3 + s4;

t1.setText(s5); }

if(e.getSource()==b4){ s3 =

t1.getText(); s4 = "4";

s5 = s3 + s4;

t1.setText(s5); }

if(e.getSource()==b5){ s3 =

t1.getText(); s4 = "5";

s5 = s3 + s4;

t1.setText(s5); }

if(e.getSource()==b6){ s3 =

t1.getText(); s4 = "6";

s5 = s3 + s4;

t1.setText(s5); }

if(e.getSource()==b7){ s3 =

t1.getText(); s4 = "7";

s5 = s3 + s4;

t1.setText(s5); }

if(e.getSource()==b8){ s3 =

t1.getText(); s4 = "8";

s5 = s3 + s4;

t1.setText(s5); }

if(e.getSource()==b9){ s3 =

t1.getText(); s4 = "9";

s5 = s3 + s4;

t1.setText(s5); }

if(e.getSource()==badd){ s1 =

t1.getText(); t1.setText("");

c = 1;

}

if(e.getSource()==bsub){ s1 =

t1.getText(); t1.setText("");

c = 2;

}

if(e.getSource()==bmul){ s1 =

t1.getText(); t1.setText("");

c = 3;

}

if(e.getSource()==bdiv){

s1 = t1.getText();

t1.setText("");

c = 4;

}

if(e.getSource()==beq){

s2 = t1.getText();

if(c==1){

n = Integer.parseInt(s1) + Integer.parseInt(s2);

t1.setText(String.valueOf(n));

}

if(c==2){

n = Integer.parseInt(s1) - Integer.parseInt(s2);

t1.setText(String.valueOf(n));

}

if(c==3){

n = Integer.parseInt(s1) * Integer.parseInt(s2);

t1.setText(String.valueOf(n));

}

if(c==4){

n = Integer.parseInt(s1) / Integer.parseInt(s2);

t1.setText(String.valueOf(n));

}

}

if(e.getSource()==bclr){

t1.setText("");

}

}

public static void main(String[] args) {

sampleex c = new sampleex();

}

}
