/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package com.mycompany.maze_solver_project;


import java.awt.Color;
import java.awt.Graphics;
import java.awt.event.KeyEvent;
import java.util.ArrayList;
import java.util.List;
import java.util.Timer;
import java.util.TimerTask;
import javax.swing.JFrame;
import javax.swing.SwingUtilities;

/**
 *
 * @author Firdoush
 */



public class NewClass extends JFrame {
    private int [][] maze=
            {{1,1,1,1,1,1,1,1,1,1,1,1,1},
                    {1,0,1,0,1,0,1,0,0,0,0,0,1},
                    {1,0,1,0,0,0,1,0,1,1,1,0,1},
                    {1,0,0,0,1,1,1,0,0,0,0,0,1},
                    {1,0,1,0,0,0,0,0,1,1,1,0,1},
                    {1,0,1,0,1,1,1,0,1,0,0,0,1},
                    {1,0,1,0,1,0,0,0,1,1,1,0,1},
                    {1,0,1,0,1,1,1,0,1,0,1,0,1},
                    {1,0,0,0,0,0,0,0,0,0,0,9,1},
                    {1,1,1,1,1,1,1,1,1,1,1,1,1}
            };
    private List<Integer> path=new ArrayList<>();
    //     private int pathIndex;
    public NewClass(){
        setTitle("Maze Solver");
        setSize(640,480);
        setLocationRelativeTo(null);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        DepthFirst.searchpath(maze,1,1,path);
        System.out.println(path);

    }

    @Override
    public void paint(Graphics g) {
        super.paint(g);
        g.translate(50, 50);

        for (int row=0;row<maze.length;row++) {
            for (int col=0;col<maze[0].length;col++) {
                Color color;
                switch(maze[row][col]) {
                    case 1 : color=Color.BLACK; break;
                    case 9 : color=Color.RED; break;
                    default : color=Color.WHITE; break;

                }
                g.setColor(color);
                g.fillRect(30*col,30*row,30,30);
                g.setColor(Color.RED);
                g.drawRect(30*col,30*row,30,30);

            }
        }
        for(int p=0;p<path.size();p+=2){
            int pathx=path.get(p);
            int pathy=path.get(p+1);
            System.out.println("path x coordinate"+pathx);
            System.out.println("path y coordinate"+pathy);
            g.setColor(Color.GREEN);
            g.fillRect(pathx*30, pathy*30, 30, 30);


        }
        
    }
      

    public static void main(String[] args){
        SwingUtilities.invokeLater(new Runnable(){
            @Override
            public void run(){
                NewClass view =new NewClass();
                view.setVisible(true);
            }

        });

    }
}

/*public class NewClass extends JFrame {
    
      private int [][] maze=
    {{1,1,1,1,1,1,1,1,1,1,1,1,1},
          {1,0,1,0,1,0,1,0,0,0,0,0,1},
          {1,0,1,0,0,0,1,0,1,1,1,0,1},
          {1,0,0,0,1,1,1,0,0,0,0,0,1},
          {1,0,1,0,0,0,0,0,1,1,1,0,1},
          {1,0,1,0,1,1,1,0,1,0,0,0,1},
          {1,0,1,0,1,0,0,0,1,1,1,0,1},
          {1,0,1,0,1,1,1,0,1,0,1,0,1},
          {1,0,0,0,0,0,0,0,0,0,0,9,1},
          {1,1,1,1,1,1,1,1,1,1,1,1,1}
    };
      
      public List<Integer> path=new ArrayList<>();
      
      
      public NewClass(){
            setTitle("Maze Solver");
        setSize(640,480);
        //setLocationRelativeTo(null);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        DefaultFirst.searchpath(maze,1,1,path);
        System.out.println(path);
        
        
        
        
      }
      
      
      @Override
       public void paint(Graphics g) {
            g.translate(50, 50);
           
             for (int i=0;i<maze.length;i++) {
            for (int j=0;j<maze[0].length;j++) {
                Color color;
                switch(maze[i][j]) {
                    case 1 : color=Color.BLACK; break;
                    case 9 : color=Color.RED; break;
                    default : color=Color.WHITE; break;
                    
                }
                
                g.setColor(color);
                g.fillRect(30*j,30*i,30,30);
                g.setColor(Color.RED);
                g.drawRect(30*j,30*i, 30, 30);
            
            }
          
          }
             
           for(int i=0;i<path.size();i+=2){
               
               int pathx=path.get(i);
               int pathy=path.get(i+1);
               
               
               System.out.println("X coordinates"+pathx);
               System.out.println("Y coordinates"+pathy);
               
               
               g.setColor(Color.GREEN);
               g.fillRect(30*pathx, 30*pathy, 20, 30);
            
               
               
           }  
             
                    
       }
       
        public static void main(String[] args){
            NewClass view =new NewClass();
                view.setVisible(true);
        }
      
    
}*/
