### Solutions
##### Solution # 1 - Manual Threshold (357 bytes)

    import javax.imageio.ImageIO;
    import java.io.File;
    public class a{
      public static void main(String[] args) throws Exception{
        java.awt.image.BufferedImage i=ImageIO.read(new File("i"));
        int x,y;
        for(x=0;x<i.getWidth();x++)for(y=0;y<i.getHeight();y++)i.setRGB(x,y,(i.getRGB(x,y)&0xFF)<128?0:16777215);
        ImageIO.write(i,"png",new File("o"));}}

This solution uses a default threshold of 128. It expects a .png file called `i` and outputs a resulting binary .png file to `o`. 

*Solution # 1 input*  
![https://raw.githubusercontent.com/anthonyjchriste/the-daily-programmer/master/challenges/1/anthonyjchriste/in.png](https://raw.githubusercontent.com/anthonyjchriste/the-daily-programmer/master/challenges/1/anthonyjchriste/in.png)

*Solution # 1 output (t=128)*  
![https://raw.githubusercontent.com/anthonyjchriste/the-daily-programmer/master/challenges/1/anthonyjchriste/out-t128.png](https://raw.githubusercontent.com/anthonyjchriste/the-daily-programmer/master/challenges/1/anthonyjchriste/out-t128.png)

##### Needed dependencies
* JDK 7 or greater