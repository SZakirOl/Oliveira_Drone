# Oliveira_Drone
Simulation using button, drone movement in x, y,z location
//Author Name: Sabina Oliveira
//Date: 05/14/2022
//Program Name: Oliveira_Drone
//Purpose: Simulation using button, drone movement in x, y,z location


import java.util.Scanner;
public class Oliveira_Drone {
    public static String [] orien = {"North", "East", "South", "West"};
    // method to show orientation in text format
    public static String generate (int orientation){
        if (orientation == 0){
            return orien[0];
        } else if (orientation == 1) {
            return orien[1];
        } else if (orientation == 2) {
            return orien[2];
        } else if (orientation == 3) {
            return orien[3];
        }
        return generate(orientation);

    }
// declare variables  for drone's coordinates
private int x, y, z;
// declare variable for orientation 0-North, 1-East, 2-South, 3-West

    private int orientation;

// create constructor

    public Oliveira_Drone() {

        x = 0;

        y = 0;

        z = 0;

        orientation = 0; // north

    }

// getters and setters for x,y, z and orientation

    public int getX() {

        return x;

    }

    public void setX(int x) {

        this.x = x;

    }

    public int getY() {

        return y;

    }

    public void setY(int y) {

        this.y = y;

    }


    public int getZ() {

        return z;

    }

    public void setZ(int z) {

        this.z = z;

    }

    public int getOrientation() {

        return orientation;

    }

    public void setOrientation(int z) {

        this.orientation = orientation;

    }

// method to move the drone up vertically on Z-axis

    public void moveUp(int spaces) {

        z+= spaces;

    }

// method to move the drone down Z-axis along

    public void moveDown(int spaces) {

        z -= spaces;


    }

// method to move forward the drone

    public void forward(int spaces) {

        if (orientation == 0) {

// move north

            y += spaces;

        } else if (orientation == 1) {

// move east

            x += spaces;

        } else if (orientation == 2) {

//  move south

            y -= spaces;

        } else {

// move west

            x -= spaces;

        }


    }

// move backward

    public void backward(int spaces) {

        if (orientation == 0) {

// move south

            y -= spaces;

        } else if (orientation == 1) {

// west

            z -= spaces;

        } else if (orientation == 2) {

// north

            y += spaces;

        } else {

// east

            z += spaces;

        }

    }

// method to turn drone 90 degrees to right

    public void turnRight(int spaces) {

        orientation = (orientation + 1) % 4;
        x+= spaces;
    }

// method to turn drone 90 degrees to left

    public void turnLeft(int spaces) {

        orientation--;

        if (orientation < 0) {

            orientation = 3;
            x-=spaces;
        }

    }

    public static String [] orien = {"North", "East", "South", "West"};
    // method to show orientation in text format
    public static String generate (int orientation){
        if (orientation == 0){
            return orien[0];
        } else if (orientation == 1) {
            return orien[1];
        } else if (orientation == 2) {
            return orien[2];
        } else if (orientation == 3) {
            return orien[3];
        }
        return generate(orientation);

    }



    @Override

    public String toString() {

// returns a string  of drone's position

        return "Student_Drone [x_pos=" + x + ", y_pos=" + y + ", z_pos=" + z + ",  orientation= " + orientation + " ]";

    }

    public static void main(String[] args) {

// create a drone

        Oliveira_Drone drone = new Oliveira_Drone();
        System.out.println(" Which direction would you like to move the drone?");



        Scanner scanner = new Scanner(System.in);

        String ch = "";

// looping until user chooses to quit

        while (!ch.equalsIgnoreCase("8")) {

// displaying drone's current position

         //  System.out.println("\n" + drone + "\n");

// displaying the menu

            System.out.println("1 - Move Up");

            System.out.println("2 - Move Down");

            System.out.println("3 - Move Forward");

            System.out.println("4 - Move Backward");

            System.out.println("5 - Turn Left");

            System.out.println("6 - Turn Right");

            System.out.println("7 - Display position");

            System.out.println("8 - Exit Navigation");



// reading option

            ch = scanner.next();

// handling choice, invoking appropriate methods in Drone class
            if (ch.equalsIgnoreCase("7")) {

               System.out.println("\n" + drone + );

           }

            if (ch.equalsIgnoreCase("1")) {

                drone.moveUp(1);
                System.out.println("You have move up");

            } else if (ch.equalsIgnoreCase("2")) {

                drone.moveDown(1);
                System.out.println("You have move down");

            } else if (ch.equalsIgnoreCase("3")) {

                drone.forward(1);
                System.out.println("You have move forward");

            } else if (ch.equalsIgnoreCase("4")) {

                drone.backward(1);
                System.out.println("You have move backward");

            } else if (ch.equalsIgnoreCase("5")) {

                drone.turnLeft(1);
                System.out.println("You have move Left");

            } else if (ch.equalsIgnoreCase("6")) {

                drone.turnRight(1);
                System.out.println("You have move right");

            }


        }

    }

}
//Author Name: Sabina Oliveira
//Date: 05/14/2022
//Program Name: Oliveira_Drone
//Purpose: Simulation using button, drone movement in x, y,z location


import java.util.Scanner;
public class Oliveira_Drone {
    public static String [] orien = {"North", "East", "South", "West"};
    // method to show orientation in text format
    public static String generate (int orientation){
        if (orientation == 0){
            return orien[0];
        } else if (orientation == 1) {
            return orien[1];
        } else if (orientation == 2) {
            return orien[2];
        } else if (orientation == 3) {
            return orien[3];
        }
        return generate(orientation);

    }
// declare variables  for drone's coordinates
private int x, y, z;
// declare variable for orientation 0-North, 1-East, 2-South, 3-West

    private int orientation;

// create constructor

    public Oliveira_Drone() {

        x = 0;

        y = 0;

        z = 0;

        orientation = 0; // north

    }

// getters and setters for x,y, z and orientation

    public int getX() {

        return x;

    }

    public void setX(int x) {

        this.x = x;

    }

    public int getY() {

        return y;

    }

    public void setY(int y) {

        this.y = y;

    }


    public int getZ() {

        return z;

    }

    public void setZ(int z) {

        this.z = z;

    }

    public int getOrientation() {

        return orientation;

    }

    public void setOrientation(int z) {

        this.orientation = orientation;

    }

// method to move the drone up vertically on Z-axis

    public void moveUp(int spaces) {

        z+= spaces;

    }

// method to move the drone down Z-axis along

    public void moveDown(int spaces) {

        z -= spaces;


    }

// method to move forward the drone

    public void forward(int spaces) {

        if (orientation == 0) {

// move north

            y += spaces;

        } else if (orientation == 1) {

// move east

            x += spaces;

        } else if (orientation == 2) {

//  move south

            y -= spaces;

        } else {

// move west

            x -= spaces;

        }


    }

// move backward

    public void backward(int spaces) {

        if (orientation == 0) {

// move south

            y -= spaces;

        } else if (orientation == 1) {

// west

            z -= spaces;

        } else if (orientation == 2) {

// north

            y += spaces;

        } else {

// east

            z += spaces;

        }

    }

// method to turn drone 90 degrees to right

    public void turnRight(int spaces) {

        orientation = (orientation + 1) % 4;
        x+= spaces;
    }

// method to turn drone 90 degrees to left

    public void turnLeft(int spaces) {

        orientation--;

        if (orientation < 0) {

            orientation = 3;
            x-=spaces;
        }

    }

    public static String [] orien = {"North", "East", "South", "West"};
    // method to show orientation in text format
    public static String generate (int orientation){
        if (orientation == 0){
            return orien[0];
        } else if (orientation == 1) {
            return orien[1];
        } else if (orientation == 2) {
            return orien[2];
        } else if (orientation == 3) {
            return orien[3];
        }
        return generate(orientation);

    }



    @Override

    public String toString() {

// returns a string  of drone's position

        return "Student_Drone [x_pos=" + x + ", y_pos=" + y + ", z_pos=" + z + ",  orientation= " + orientation + " ]";

    }

    public static void main(String[] args) {

// create a drone

        Oliveira_Drone drone = new Oliveira_Drone();
        System.out.println(" Which direction would you like to move the drone?");



        Scanner scanner = new Scanner(System.in);

        String ch = "";

// looping until user chooses to quit

        while (!ch.equalsIgnoreCase("8")) {

// displaying drone's current position

         //  System.out.println("\n" + drone + "\n");

// displaying the menu

            System.out.println("1 - Move Up");

            System.out.println("2 - Move Down");

            System.out.println("3 - Move Forward");

            System.out.println("4 - Move Backward");

            System.out.println("5 - Turn Left");

            System.out.println("6 - Turn Right");

            System.out.println("7 - Display position");

            System.out.println("8 - Exit Navigation");



// reading option

            ch = scanner.next();

// handling choice, invoking appropriate methods in Drone class
            if (ch.equalsIgnoreCase("7")) {

               System.out.println("\n" + drone + );

           }

            if (ch.equalsIgnoreCase("1")) {

                drone.moveUp(1);
                System.out.println("You have move up");

            } else if (ch.equalsIgnoreCase("2")) {

                drone.moveDown(1);
                System.out.println("You have move down");

            } else if (ch.equalsIgnoreCase("3")) {

                drone.forward(1);
                System.out.println("You have move forward");

            } else if (ch.equalsIgnoreCase("4")) {

                drone.backward(1);
                System.out.println("You have move backward");

            } else if (ch.equalsIgnoreCase("5")) {

                drone.turnLeft(1);
                System.out.println("You have move Left");

            } else if (ch.equalsIgnoreCase("6")) {

                drone.turnRight(1);
                System.out.println("You have move right");

            }


        }

    }

}
