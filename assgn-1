import java.io.*;
import java.util.*;
import java.util.regex.Pattern;

class Listoffiles
{
    public void matching(String reg,String path) throws NullPointerException
    {
        File f = new File(path);
        if(!f.exists())
        {
            return;
        }
        File [] allsubfiles = f.listFiles();
        for(File subfile : allsubfiles)
        {
            if(subfile.isDirectory())
            {
                matching(reg,subfile.getAbsolutePath());  // Recursive call if it is a directory, to check the files inside it.
            }
            else
            {
                String filename=subfile.getName();
                if(Pattern.matches(reg,filename))
                {
                    System.out.println(subfile.getAbsolutePath());
                }
            }
        }
    }
}
class Main
{
    public static void main(String args[]) throws NullPointerException
    {
        Listoffiles lo = new Listoffiles();
        lo.matching("*.txt","/home");
    }
}
