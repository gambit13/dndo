dndo
====
import java.applet.*;
import java.awt.*;

public class Beginning extends Applet
{
	
	Image bckground,upper;
	Label intro;
	Font f=new Font("Helvetica",1,20);
	public void init()
    {
		intro=new Label("");
		setSize(1900,1000);
		bckground=getImage(getDocumentBase(),"dond1.jpg");
		upper=getImage(getDocumentBase(),"upper.jpg");
    }

//This method gets called when the applet is terminated
//That's when the user goes to another page or exits the browser.
	public void stop()
    {
 // no actions needed here now.
    }

//The standard method that you have to use to paint things on screen
	public void paint(Graphics g)
    {
		g.drawImage(bckground, 0, 0, this);
		g.drawImage(upper, 770, 1, this);
		intro.setBounds(300, 200, 1000, 50);
		intro.setForeground(Color.RED);
		intro.setFont(f);
		intro.setText("Welcome Player! Please enter to your name.");
		add(intro);
    }
}
