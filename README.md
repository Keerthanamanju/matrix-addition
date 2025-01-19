# matrix-addition
import java.util.Scanner;


public class MatrixAddition {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        // Input the dimensions of the matrices
        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();
        System.out.print("Enter the number of columns: ");
        int columns = scanner.nextInt();


        // Create two matrices
        int[][] matrix1 = new int[rows][columns];
        int[][] matrix2 = new int[rows][columns];
        int[][] resultMatrix = new int[rows][columns];


        // Input elements for the first matrix
        System.out.println("Enter elements for the first matrix:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                System.out.print("Matrix1[" + i + "][" + j + "]: ");
                matrix1[i][j] = scanner.nextInt();
            }
        }


        // Input elements for the second matrix
        System.out.println("Enter elements for the second matrix:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                System.out.print("Matrix2[" + i + "][" + j + "]: ");
                matrix2[i][j] = scanner.nextInt();
            }
        }


        // Perform matrix addition
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                resultMatrix[i][j] = matrix1[i][j] + matrix2[i][j];
            }
        }


        // Display the result of the matrix addition
        System.out.println("\nResultant Matrix after addition:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                System.out.print(resultMatrix[i][j] + " ");
            }
            System.out.println();
        }


        // Close the scanner
        scanner.close();
    }
}


OUTPUT:


Enter the number of rows: 2
Enter the number of columns: 3
Enter elements for the first matrix:
Matrix1[0][0]: 1
Matrix1[0][1]: 2
Matrix1[0][2]: 3
Matrix1[1][0]: 4
Matrix1[1][1]: 5
Matrix1[1][2]: 6
Enter elements for the second matrix:
Matrix2[0][0]: 7
Matrix2[0][1]: 8
Matrix2[0][2]: 9
Matrix2[1][0]: 10
Matrix2[1][1]: 11
Matrix2[1][2]: 12


Resultant Matrix after addition:
8 10 12 
14 16 18 
