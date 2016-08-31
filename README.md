
/*public class Task {
	public static void main(String[] args) {
		for ( int x = 1 ; x <= 9 ; x ++ ){
			for ( int y = 1 ; y <= x ; y ++ ){
				System.out.print( y + " * " + x + " = " + (x * y) + "\t");
			}System.out.println();
		}
	}
}*//*
public class Task{
	public static void main(String[] args){
		System.out.println("100 - 999之间所有无重复的3位数如下：");
		for ( int X = 100 ; X <= 999 ; X ++ ){
			int a = X % 10;     //取个位数字
			int temp = X / 10;
			int b = temp % 10;  //取十位数字
			 temp = temp / 10;
			int c = temp;       //取百位数字
			if ( a == b || b == c || a == c){  //比较个、十、百位数字是否重复
				continue;
			}else
				System.out.println( X );
		}
	}
}*/
/*
import java.util.Scanner;

public class Task{
	public static void main(String[] args){
		System.out.println("请输入菱形边长：");    //输入菱形边长
		Scanner scan = new Scanner(System.in);
		int m = scan.nextInt();
		int n = 2 * m;
		for ( int x = 1 ; x <= n ; x ++ ){    //执行菱形行数
			for ( int i = 1 ; i < m ; i ++ ){ //执行每行空格
				System.out.print( " ");
			}
			for ( int j = 0 ; j <= n/2 - m ; j ++ ){ //打印每行的 *
				System.out.print("*" + " ");
			}
			System.out.println();
			if ( x < n/2)    //菱形取中转折
				m--;
			else
				m++;
		}scan.close();
	}
}*//*
public class Task{
	public static void main(String[] args) {
		move(10);
		System.out.println("增加速度：" + speedUp(25,10) + " 米。");
		System.out.println("减少速度：" + speedDown(25,10) + " 米。");
	}
	
	public static void move(int x) {            //移动速度
		System.out.println("移动了 " + x + " 米。");	
	}
	
	public static int speedUp(int x,int y) {     //增加速度
		return x + y;
	}
	
	public static int speedDown(int x,int y) {   //减少速度
		return x - y;
	}
}*/
/*
class People{
	//封装信息属性
	private String name;
	private int age;
	private String sex;
	private double weight;
	public People() { }          //构造无参方法
	public People(String name,int age,String sex){  //构造部分（姓名、年龄、性别）参数方法
		this.name = name;
		this.age = age;
		this.sex = sex;
	}
	public People(String name,int age,String sex,double weight){  //构造全部参数方法
		//setName(name);         //
		this.name = name;
		//setAge(age);           //
		this.age = age;
		//setSex(sex);           //
		this.sex = sex;
		//setWeight(weight);     //
		this.weight = weight;
	}
	
	public void setName(String name){
		this.name = name;
	}
	public void setAge(int age){
		if(age > 0)
			this.age = age;
		else
			this.age = 0;
	}
	public void setSex(String sex){
		this.sex = sex;
	}
	public void setWeight(double weight){
		if(weight > 0.0){
			this.weight = weight;
		}else
			this.weight = 0.0;
	}
	
	public String getName(){
		return this.name;
	}
	public int getAge(){
		return this.age;
	}
	public String getSex(){
		return this.sex;
	}
	public double Weight(){
		return this.weight;
	}
	
	public String printInfo(){
		return "姓名： " + this.name + ";  年龄： " + this.age + 
				";  性别： " + this.sex + ";  体重： "+ this.weight;
	}
}

public class Task{  //TestDemo
	public static void main(String[] args) {
		People people = new People("TOMAS",56,"男",65.8);  //对象实例化
		System.out.println(people.printInfo());           //打印结果
		
		People peop = new People("MISS",25,"女");
		peop.setWeight(56.2);
		System.out.println(peop.printInfo());
	}
}*/
/*
class Car{
	//封装信息属性 / 品牌、颜色、型号、速度
	private String brand;
	private String color;
	private String model;
	private double speed;
	public Car(){ }
	public Car(String brand,String color,String model,double speed){  //构造全部属性参数方法
		this.brand = brand; //setBrand(brand);
		this.color = color; //setColor(color);
		this.model = model; //setModel(model);
		this.speed = speed; //setSpeed(speed);
	}
	
	public void setBrand(String brand){
		this.brand = brand;
	}
	public void setColor(String color){
		this.color = color;
	}
	public void setModel(String model){
		this.model = model;
	}
	public void setSpeed(double speed){
		this.speed = speed;
	}
	
	public String getBrand(){
		return this.brand;
	}
	public String getColor(){
		return this.color;
	}
	public String getModel(){
		return this.model;
	}
	public double getSpeed(){
		return this.speed;
	}
	
	public static double speedUp(double speed){ //完成加速
		return speed + 10;
	}
	public static double speedDown(double speed){ //完成减速
		return (speed-10 >= 0)? speed-10 : 0;
	}
	
	public String printInfo(){ //返回输出
		return "汽车品牌： " + brand + "；  颜色： " + color + "；  型号 ： " +
			model + "；  速度： " + speed + "\n 加速后为： " + 
		speedUp(this.speed) + ";  减速后为： " + speedDown(this.speed);
	}
}

public class Task{
	public static void main(String[] args) {
		Car car = new Car("宝马","银白","宝马750",65.0);     //对象实例化
		System.out.println(car.printInfo());   //实现输出
	}
}*/
/*
public class Task{
	public static void main(String[] args) {
		int num[] = new int[10];
		System.out.print("数组中的数据为：[");
		for(int i = 0;i < num.length;i ++){
			num[i] = (int)(Math.random()*100);
			System.out.print(num[i] + " ");
		}System.out.println("]");
		max(num);
	}
public static void max(int arr[]){
	int temp = arr[0];
	for(int i = 0;i < arr.length;i ++){
		if(temp < arr[i]){
			temp = arr[i];
			}
		}
	System.out.println("最大值是：" + temp);
	}
}*//*
public class Task{
	public static void main(String[] args) {
		int num[] = new int[10];
		System.out.print("原数组中的数据为：");
		for(int i = 0;i < num.length;i ++){
			num[i] = (int)(Math.random()*100);
			System.out.print(num[i] + "\t");
		}
		reverse(num);
	}
public static void reverse(int arr[]){
	for(int i = 0;i < arr.length/2;i ++){
		int temp = arr[i];
		arr[i] = arr[arr.length - 1 - i];
		arr[arr.length - 1 - i] = temp;
		}System.out.print("\n数组倒序输出为 ：  ");
		for(int i = 0;i < arr.length;i ++){
			System.out.print(arr[i] + "\t");
			}
		}
}*/
/*
public class Task{
	public static void main(String[] args) {
		int num[] = new int[10];
		System.out.print("原数组中的数据为：");
		for(int i = 0;i < num.length;i ++){
			num[i] = (int)(Math.random()*100);
			System.out.print(num[i] + "\t");
		}
		sort(num);
	}
public static void sort(int arr[]){     //创建冒泡排序方法
	for(int i = 0;i < arr.length;i ++){
		for(int j = 0;j < arr.length - 1;j ++){  //冒泡排序
			if(arr[j] > arr[j + 1]){
				int temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
				}
			}
		}System.out.print("\n排序后数组为：");
	for(int i = 0;i < arr.length;i ++){
		System.out.print(arr[i] + "\t");
	}
	}
}*/
/*
import java.util.Scanner;
interface UnionPay{             //银联接口
	public boolean checkPwd(String input);       //检测密码
	public boolean drawMoney(double number);    //取钱
	public double getBalance(); //查询余额
}

interface ICBC extends UnionPay{  //工商银行接口
	public void payOnline(double number);      //在线支付
}

interface ABC extends UnionPay{  //农业银行接口
	public boolean payPhoneBill(String poneNum,double sum);  //支付话费
	//public void overdraw();      //透支
}

class ICBCImpl implements ICBC{
	private double money;
	private String pwd;
	
	public ICBCImpl(double money,String pwd){
		this.money = money;
		this.pwd = pwd;
	}
	public boolean checkPwd(String input){
		if(pwd.equals(input)){
			return true;
		}
		return false;
	}
	public boolean drawMoney(double number){
		if(number <= money){
			money -= number;
			return true;
		}
		return false;
	}
	public double getBalance(){
		return money;
	}
	public void payOnline(double number){
		if(number <= money){
			money -= number;
		}
	}
}

class ABCImpl implements ABC{
	private double balance;
	private String password;
	
	public ABCImpl(double balance,String password){
		this.balance = balance;
		this.password = password;
	}
	public boolean drawMoney(double number){
		if(balance - number >= -2000){
			balance -= number;
			return true;
		}
		return false;
	}
	public boolean checkPwd(String input){
		if(password.equals(input)){
			return true;
		}
		return false;
	}
	 public boolean payPhoneBill(String phoneNum,double sum){
		 if(phoneNum.length() == 11 && (balance - sum) >= -2000){
			 balance -= sum;
			 return true;
		 }
		 return false;
	 }
	 public double getBalance(){
		 return balance;
	 }
}
public class Task{
	public static void main(String[] args) {
		UnionPay icbc = new ICBCImpl(2000,"123456");  //卡内余额为：2000，密码为：123456
		Scanner input = new Scanner(System.in);
		System.out.println("测试工商银行卡:  \n  请输入银行卡密码：");
		if(icbc.checkPwd(input.next())){
			System.out.println("  请输入要取金额：");
			double sum = input.nextDouble();
			if(icbc.drawMoney(sum)){
				System.out.println("  取款成功，余额为：" + icbc.getBalance());
			}else
				System.out.println("  取款失败,余额为：" + icbc.getBalance());
		}else
			System.out.println("  密码输入错误。");
		input.close();
	}
}*/
/*
class Emperor{
	private static final Emperor EMPEROR = new Emperor();   //实例化类对象
	private Emperor(){}   //构造方法私有化
	public static Emperor getInstance(){
		return EMPEROR;
	}
	public void print(){
		System.out.println("古代皇帝：秦始皇");
	}
}
public class Task{
	public static void main(String[] args) {
		Emperor emperor = null;  //声明对象
		emperor = Emperor.getInstance();
		emperor.print();
	}
}*/
/*
public class Task{
	public static void main(String[] args){
		int i,j,k,g;
		for(i=1;i<6;i++){
			for(j=1;j<=6-i;j++)
				System.out.print(" ");
			for(k=1;k<=i;k++){
				for(g=1;g<=1;g++)
					System.out.print(" ");
				System.out.print("*");
			}
			System.out.println();
		}
		for(i=6;i>=1;i--){
			for(j=1;j<=6-i;j++)
				System.out.print(" ");
			for(k=1;k<=i;k++){
				for(g=1;g<=1;g++)
					System.out.print(" ");
				System.out.print("*");
			}
			System.out.println();
		}
	}
}*/
/*
abstract class Pet{
	double weight;
	String color;
	public abstract void act();
}

class Cat extends Pet{
	public Cat(double weight,String color){
		this.weight = weight;
		this.color = color;
	}
	public void act(){
		System.out.println("猫,体重：" + this.weight + ", 颜色：" + this.color+", 会爬树。");
	}
}
class Dog extends Pet{
	public Dog(double weight,String color){
		this.weight = weight;
		this.color = color;
	}
	public void act(){
		System.out.println("狗,体重：" + this.weight + ", 颜色：" + this.color+", 会游泳。");
	}
}
public class Task{
	public static void main(String[] args) {
		Pet cat = new Cat(4.65,"black");
		cat.act();
		Pet dog = new Dog(14.2,"white");
		dog.act();
	}
}*/
/*
abstract class Pet{      //Pet抽象类
	private double weight;
	private String color;
	public Pet(double weight,String color ){
		this.weight = weight;
		this.color = color;
	}
	 public void fun(){
		 System.out.println(" 体重：" + this.weight + ", 颜色：" + this.color);
	 }
	 public abstract void act();      //act抽象方法
}

class Cat extends Pet{             //猫类继承
	public Cat(double weight,String color){
		super(weight,color);
		}
	public void act(){
		System.out.print("猫  特长：爬树,"); 
		this.fun();
	}
}

class Dog extends Pet{            //狗类继承
	public Dog(double weight,String color){
		super(weight,color);
		}
	public void act(){
		System.out.print("狗  特长：游泳,"); 
		this.fun();
		}
}

public class Task{
	public static void main(String[] args){
		Pet cat=new Cat(4.6,"black");        //实例化
		cat.act();
		Pet dog=new Dog(12.2,"white");
		dog.act();
	}
}*/
/*
public class Task{
	public static void main(String[] args) {
		String str = "abc";
		System.out.println("字符串 ：" + str + " 反转后为：" + Invert(str));
	}
	
	public static String Invert(String str){
		char data[] = str.toCharArray();
		for(int i = 0;i < data.length/2;i ++){
			char temp = data[i];
			data[i] = data[data.length - 1 - i];
			data[data.length - 1 - i] = temp;
		}
		return new String(data);
	}
}*/
/*
public class Task{
	public static void main(String[] args) {
		String str = "1:张三,2:李四,3:王五";
		String result[] = str.split(",");
		for(int i = 0;i < result.length;i ++){
			String name[] = result[i].split(":");
			System.out.println("学号：" + name[0] + ",姓名：" + name[1]);
		}
	}
}*/
public class Task{
	public static void main(String[] args) {
		String str = "edcfaivobspuiodjmvajczbloap";
		char ch = 'a';
		System.out.println("该字符串中 “" + ch + "” 出现了 " + num(str,ch) + " 次");
	}
	
	public static int num(String str,char ch){
		int num = 0;
		char data[] = str.toCharArray();
		for(int i = 0;i < data.length;i ++){
			if(data[i] == ch){
				num ++;
			}
		}
		return num;
	}
}
