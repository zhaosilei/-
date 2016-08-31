# -
gjhmj
package Test01;

public class People 
{
    private String name;
    private int age; 
    private char sex;
    private float weight;
    public void SetName(String n)
    {
        name=n;
    }
    public String getName()
    {
        return name;
    }
    public void setAge(int a)
    {
        age=a;
    }
    public int getAge()
    {
        return age;
    }
    public void setSex(char s)
    {
        sex=s;
    }
    public char getSex()
    {
        return sex;
        
    }
    public void setWeight(float w )
    {
        weight=w;
    }
    public float getWeight()
    {
        return weight;
    }
    public People(){}
    public People(String name)
    {
        name="Tom";
    }
    public People(String name,int age,char sex,float weight){}
    public void printInfo()
    {
        People p=new People();
        System.out.println("姓名"+p.name+"年龄"+p.age+"性别"+p.sex+"体重"+p.weight);
    }
    public static void main(String[] args) {
        // TODO Auto-generated method stub

    }

}

