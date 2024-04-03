import java.util.Scanner;
public class Main{
    static int balance=0;
    static int withdraw;
    static int deposit;
Scanner sc=new Scanner(System.in);
public void Id()
{     int userId;
      String password;
      System.out.println("For new user please make user id and password !");
      System.out.println("Enter USER Id : ");
      userId=sc.nextInt();
      System.out.println("Enter the password : ");
      password=sc.next();
}

public void depositt()
{
    // int deposit;
     System.out.println("Enter the amount you want to deposit : ");
     deposit=sc.nextInt();
     balance=balance+deposit;
     System.out.println("Deposit of " +deposit+ " Rs successfully done!");
    
}
public void withdraww()
{
    //int withdraw;
    System.out.println("Enter the amount you want to withdraw : ");
    withdraw=sc.nextInt();
    balance=balance-withdraw;
    System.out.println("Withdraw of " +withdraw+ "Rs successfully done!");
}
public void transactionHistory()
{
    System.out.println("Withdrawn money:"+  withdraw);
    System.out.println("Deposited money:"+ deposit);
}

public static void main(String []args)
{     Scanner sc=new Scanner(System.in);
      System.out.println("//......Welcome to ATM.....//");
      System.out.println("");
      Main obj=new Main();
      System.out.println("");
      obj.Id();
      
     
      while(true)
      {
           System.out.println("Press 1 for Withdraw");
           System.out.println("Press 2 for Deposit");
           System.out.println("Press 3 for Check balance");
           System.out.println("Press 4 for transaction history");
           System.out.println("Press 5 for exit");
           
      
      int choice=sc.nextInt();
      switch(choice)
      {
          case 1://withdrwan
              if(balance>=1)
              {
                  obj.withdraww();
                  //balance=balance-withdraw;
              }
              else
              {
                System.out.println("Oops...Insufficient balance...");
              }
             System.out.println("");
             break;
             
          case 2://deposit
         
          obj.depositt();
          //balance=balance+deposit;
          System.out.println("");
          break;
          
          case 3://check balance
           System.out.println("Your balance is : " +balance);
           System.out.println("");
           break;
           case 4://transaction history
           System.out.println("Transaction History.....");
           System.out.println("");
           obj.transactionHistory();
           System.out.println("");
           break;
           case 5://Exit
            System.out.println("Now you can exit from this screen...Thank you!!");
            System.exit(0);
            
      }
      }
     
}}
