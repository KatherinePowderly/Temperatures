# Temperatures

public class temperatures {


    public static void main(String[] args) {
        int grid[][] = {{68, 70, 76, 70, 68, 71, 75},
                {76, 76, 87, 84, 82, 75, 83},
                {73, 72, 81, 78, 76, 73, 77},
                {64, 65, 69, 68, 70, 74, 72}};


        System.out.println("The data provided are:");
        int[][] temps = new int[4][7];
        temps[0][0] = 68;
        temps[3][6] = 72;


        String[] time = new String[]{"7AM:", "3PM:", "7PM:", "3AM:"};
        time[0] = "7AM:";
        time[3] = "3AM:";

        String[] day = new String[]{"Sun", "Mon", "Tues", "Wed", "Thurs", "Fri", "Sat"};
        day[0] = "Sun:";
        day[6] = "Sat:";


        /* chart */

        for (int row = 0; row < 4; row++) {

            System.out.println("----");
            System.out.print(time[row]);
            System.out.print("\t" + "|" + row + "|" + "\t");

            for (int column = 0; column < 7; column++) {


                System.out.print("\t");
                System.out.print(grid[row][column]);


            }
            System.out.println();

        }
        System.out.println("\n" + "Based on that data, the following are the average temperatures for the week." + "\n");

        /* avg temps of week */

        for (int column = 0; column < 7; column++) {

            int sum = 0;
            System.out.print(day[column] + " ");

            for (int row = 0; row < 4; row++) {


                sum += grid[row][column];


            }
            float average = sum / (float) 4;
            System.out.println(average);
        }
        System.out.println();



        /* avg temp of day */


        for (int row = 0; row < 4; row++) {

            int sum = 0;
            System.out.print(time[row] + " ");

            for (int column = 0; column < 7; column++) {


                sum += grid[row][column];


            }
            float average = sum / (float) 7;
            System.out.println(average);
        }
        System.out.println();

        /*sum */

        float sum = 0;
        for (int index = 0; index < grid.length; index++)
        {
            sum += grid[index][index];
        }

        float average = sum / (float)grid.length;
        System.out.println("The final average temperature of the week was: " );
        System.out.println("Overall: " + average);



    }
}
