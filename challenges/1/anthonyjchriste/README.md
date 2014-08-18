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

##### Needed dependencies
* JDK 7 or greater