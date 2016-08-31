# -
gjhmj
package Bank;
interface Yinlian
{
    int password();
    int getMonny();
    int balance();
}

public class Bank 
{
    class ICBC implements Yinlian
    {

        @Override
        public int password() {
            // TODO Auto-generated method stub
            return 0;
        }

        @Override
        public int getMonny() {
            // TODO Auto-generated method stub
            return 0;
        }

        @Override
        public int balance() {
            // TODO Auto-generated method stub
            return 0;
        }
        public int Online()
        {
            return 0;
        }
        class ABC implements Yinlian
        {

            @Override
            public int password() {
                // TODO Auto-generated method stub
                return 0;
            }

            @Override
            public int getMonny() {
                // TODO Auto-generated method stub
                return 0;
            }

            @Override
            public int balance() {
                // TODO Auto-generated method stub
                
                return 0;
            }
            public int telBill(){
                return 0;
            }
             public int leftMoney(int money)
             {
                 if(money>-2000)
                     return money;
                 else
                     return -2001;
             }
            
        }
        
    }



    public static void main(String[] args) 
    {
        // TODO Auto-generated method stub

    }

}
