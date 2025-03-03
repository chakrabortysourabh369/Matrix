# Matrix
matrix codes

import java.util.*;
public class matrix{

    public static void printarray(int arr[][]){

        for(int i=0;i<arr.length;i++){

            for(int j=0;j<arr[i].length;j++){

                System.out.println(arr[i][j]);
            }
        }
    }
    //snake pattern

    public static void snakepattern(int arr[][]){

        int r=4,c=4;

        for(int i=0;i<r;i++){

            if(i%2==0){
                for(int j=0;j<c;j++){

                    System.out.print( arr[i][j] );
                }
            }
            else{
                for(int j=c-1;j>=0;j--){
                    System.out.print( arr[i][j] );
                }
            }
                System.out.println();
        }
    }

       //Transpose matrix  (efficient approach)
                        
       static int n = 4;
	static void swap(int mat[][], int i, int j)
	{
			int temp = mat[i][j];
			mat[i][j] = mat[j][i];
			mat[j][i] = temp;
	}
	static void transpose(int mat[][])
	{
		for(int i = 0; i < n; i++)
			for(int j = i + 1; j < n; j++)
				swap(mat, i, j);
	}

    //rotate matrix 90 degree

    public static void rotate(int mat[][]){

        int temp[][]=new int[n][n];
        int n=4;

        for(int i=0;i<n;i++)
             for(int j=0;j<n;j++)
                temp[n-j-1][i]=mat[i][j];
             
        
        for(int i=0;i<n;i++)
            for(int j=0;j<n;j++)
                mat[i][j]=temp[i][j];
            
        
    }
        public static void main(String args[]){
        int arr[][]={{1,2,3,4},
                    {5,6,7,8},
                    {9,10,11,12},
                    {13,14,15,16}};           
                                   
        // printarray(arr);
            //   snakepattern(arr);

          ///  transpose(arr);
          rotate(arr);
          int n=4;
            for(int i = 0; i < n; i++)
			{
				for(int j = 0; j < n; j++)
				{
					System.out.print(arr[i][j]+" ");
				}
				System.out.println();
			}	
    }
}

