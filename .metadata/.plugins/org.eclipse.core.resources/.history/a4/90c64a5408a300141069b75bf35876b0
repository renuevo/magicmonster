import java.awt.BorderLayout;
import java.awt.Color;
import java.awt.EventQueue;
import java.awt.FlowLayout;
import java.awt.Image;
import javax.swing.ImageIcon;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.JTextField;

import java.awt.Font;



import java.awt.Point;
import java.awt.event.MouseEvent;
import java.awt.event.MouseListener;
import java.awt.event.MouseMotionListener;


public class jarvis {

	private JFrame frame;
	private JButton ironMask;
	private ImageIcon ironMaskNormal;
	private ImageIcon ironMaskBye;
	private JTextField textField;
	static Point  mouseDownCompCoords;
	private JPanel panel;
	private JPanel panel_1;
	private JPanel panel_2;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {

		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
			        jarvis window = new jarvis();
					window.frame.setVisible(true);

				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});

	}

	/**
	 * Create the application.
	 */
	public jarvis() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.setUndecorated(true);
		frame.getContentPane().setBackground(Color.black);
	    panel = new JPanel(new FlowLayout()); // text box
		panel_1 = new JPanel(new FlowLayout(FlowLayout.LEFT, 5, 5));  //display
		panel_2 = new JPanel(new FlowLayout(FlowLayout.CENTER,5,100)); //iron mask
		
		///////panel setting (text box)
		textField = new JTextField();
		textField.setFont(new Font("HY¼¾½ºL", Font.PLAIN, 12));
		textField.setForeground(new Color(34, 139, 34));
		textField.setBorder(javax.swing.BorderFactory.createEmptyBorder());
		textField.setOpaque(false);
		textField.setColumns(10);
		panel.add(textField);
		panel.setOpaque(false);
		frame.getContentPane().add(panel,BorderLayout.SOUTH);
		/////////////////////////////////////////////////////////////////////////////////////////////////////
		
		///////panel_1 setting (display)
		panel_1.setOpaque(false);
		/////////////////////////////////////////////////////////////////////////////////////////////////////
		
		///////panel_2 setting (iron mask)
		//mask button create
		ironMask = new JButton();
		ironMaskNormal = new ImageIcon(getClass().getResource("/res/image/IronManMask.png"));
		Image resize = ironMaskNormal.getImage();
		ironMaskNormal = new ImageIcon(resize.getScaledInstance(100,100,java.awt.Image.SCALE_SMOOTH));
		
		ironMaskBye = new ImageIcon(getClass().getResource("/res/image/IronManMaskBye.png"));
	    resize = ironMaskBye.getImage();
	    ironMaskBye = new ImageIcon(resize.getScaledInstance(100,100,java.awt.Image.SCALE_SMOOTH));

		//set button image
		ironMask.setIcon(ironMaskNormal);  
		ironMask.setBorderPainted(false);  
		ironMask.setFocusPainted(false);  
		ironMask.setContentAreaFilled(false); 
		
		panel_2.setOpaque(false);
		panel_2.add(ironMask);
		/////////////////////////////////////////////////////////////////////////////////////////////////////
		
		
		//add panel
		frame.getContentPane().add(panel, BorderLayout.SOUTH);		//text
		frame.getContentPane().add(panel_1, BorderLayout.CENTER);	//display
		frame.getContentPane().add(panel_2, BorderLayout.WEST);		//maskbutton
		
		
		frame.setBounds(100, 100, 450, 300);
		
		
		
		
		//event
		initEvent();
		
	}
	
	////////////////////////////event
	
	private void initEvent()
	{
		
		//exit event
		this.ironMask.addMouseListener(new MouseListener() {
			
			@Override
			public void mouseReleased(MouseEvent e) {
				// TODO Auto-generated method stub
			}
			
			@Override
			public void mousePressed(MouseEvent e) {
				// TODO Auto-generated method stub
				
			}
			
			@Override
			public void mouseExited(MouseEvent e) {
				// TODO Auto-generated method stub
				ironMask.setIcon(ironMaskNormal);
				
			}
			
			@Override
			public void mouseEntered(MouseEvent e) {
				// TODO Auto-generated method stub
				ironMask.setIcon(ironMaskBye);
				
			}
			
			@Override
			public void mouseClicked(MouseEvent e) {
				System.exit(0);
				
			}
		});//exit event
		
		
		
		
		//drag event
		this.frame.addMouseListener(new MouseListener(){
			public void mouseReleased(MouseEvent e) {
				mouseDownCompCoords = null;
			}
			public void mousePressed(MouseEvent e) {
				mouseDownCompCoords = e.getPoint();
			}
			public void mouseExited(MouseEvent e) {
			}
			public void mouseEntered(MouseEvent e) {
			}
			public void mouseClicked(MouseEvent e) {
			}
		});

		this.frame.addMouseMotionListener(new MouseMotionListener(){
			public void mouseMoved(MouseEvent e) {
			}

			public void mouseDragged(MouseEvent e) {
				Point currCoords = e.getLocationOnScreen();
				frame.setLocation(currCoords.x - mouseDownCompCoords.x, currCoords.y - mouseDownCompCoords.y);
			}
		});
		//drag event

	}
	
}
