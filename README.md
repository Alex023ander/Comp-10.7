# Comp-10.7

import java.util.concurrent.TimeUnit;
public class Comp107 {

    public static void main(String[] args) throws InterruptedException{
        final int LINE=5,SPACE=10;
        String[] list= new String[LINE];
        for(int i=0;i<LINE;i++){
            list[i]="";
            for(int j=0;j<(int)(Math.random()*LINE)+1;j++)
            list[i]+="-";
            }
        
        for (String list1 : list) {
            System.out.println(list1);
            }
        
        for(int i=0;i<list.length;i++){
            for(int p=0;p<SPACE;p++){
                System.out.println("");
                } 
            
            TimeUnit.MILLISECONDS.sleep(2000);
            int index=i;
            String key=list[i];
            while (0<index&&key.compareTo(list[index-1])<0  ){
                list[index]=list[index-1];
                index--;
            }
            
            list[index]=key;
            for(int p=0;p<list.length;p++){
                System.out.println(list[p]);
            if(p!=list.length-1&p==i)
                }
        }
        //new line and output
        for(int p=0;p<SPACE;p++){
                System.out.println("");
                } 
        for (String list1 : list){
            System.out.println(list1);
            }
        
    }
    
}
