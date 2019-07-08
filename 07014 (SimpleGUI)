package com.company;

import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class SimpleGUI extends JFrame {
	private JButton sum = new JButton("Summation");
	private JButton sub = new JButton("Subtraction");
	private JButton del = new JButton("Delete");
	private JTextField input = new JTextField("", 5);
	private JLabel firstlabel = new JLabel("Input first number: ");
	private JLabel secondlabel = new JLabel("Input second number: ");
	Scanner num = new Scanner(System.in);
	int first, second, resultsum, resultsub;
	first = num.nextInt();
	second = num.nextInt();
	resultsum = first + second;
	resultsub = first - second;
	
	public SimpleGUI () {
		super("Plus&Minus");
		this.setBounds(100, 100, 250, 100);
		this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		
		Container container = this.getContentPane();
		container.setLayout(new GridLayout(3, 2, 2, 2));
		container.add(firstlabel);
		container.add(secondlabel);
		container.add(input);
		
		sum.addActionListener(new SumEventListener ());
		container.add(sum);
		sub.addActionListener(new SubEventListener ());
		container.add(sub);
		del.addActionListener(new DelEventListener ());
		container.add(del);
		
	}
	
	class SumEventListener implements ActionListener {
		public void actionPerformed (ActionEvent sm) {
			String message = "";
			message += "Summation is " + resultsum;
			JOptionPane.showMessageDialog(null, message, "Output", JOptionPane.PLAIN_MESSAGE);
		}
	}
	
	class SubEventListener implements ActionListener {
		public void actionPerformed (ActionEvent sb) {
			String message = "";
			message += "Subtraction is " + resultsub;
			JOptionPane.showMessageDialog(null, message, "Output", JOptionPane.PLAIN_MESSAGE);
		}
	}
	
	class DelEventListener implements ActionListener {
		public void actionPerformed (ActionEvent d) {
			firstlabel.setText(null);
			secondlabel.setText(null);
		}
	}
	
}
