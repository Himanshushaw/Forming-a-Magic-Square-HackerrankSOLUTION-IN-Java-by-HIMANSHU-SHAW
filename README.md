# Forming-a-Magic-Square-HackerrankSOLUTION-IN-Java-by-HIMANSHU-SHAW
Forming a Magic Square Hackerrank SOLUTION IN Java by HIMANSHU SHAW

import java.util.Scanner;
public class magic_square {
    public static void main(String[]args){
        Scanner sc=new Scanner(System.in);
        int[][][] Possible_matrix= {
                {{8, 1, 6}, {3, 5, 7}, {4, 9, 2}},// 1

                {{6, 1, 8}, {7, 5, 3}, {2, 9, 4}},// 2

                {{4, 9, 2}, {3, 5, 7}, {8, 1, 6}},// 3

                {{2, 9, 4}, {7, 5, 3}, {6, 1, 8}},// 4

                {{8, 3, 4}, {1, 5, 9}, {6, 7, 2}},// 5

                {{4, 3, 8}, {9, 5, 1}, {2, 7, 6}},// 6

                {{6, 7, 2}, {1, 5, 9}, {8, 3, 4}},// 7

                {{2, 7, 6}, {9, 5, 1}, {4, 3, 8}},// 8
        };
        int s[][]=new int[3][3];
        for (int i=0;i<3;i++){
            for (int j=0;j<3;j++){
                s[i][j]=sc.nextInt();
            } }
       int min_cost=Integer.MAX_VALUE;
        for (int check_permutation=0;check_permutation<8;check_permutation++){
            int sum=0;
            for (int i=0;i<3;i++){
                for (int j=0;j<3;j++){
                    sum+=Math.abs(s[i][j]-Possible_matrix[check_permutation][i][j]);
                }
            }
          min_cost=Math.min(min_cost,sum);
        }
        System.out.println(min_cost);
    }
}
