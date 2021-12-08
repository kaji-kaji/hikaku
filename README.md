import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int m = sc.nextInt();
        int n = sc.nextInt();
        int[][] a = new int[m][n];
        
        for(int i = 0; i < m; i++){
            for(int j = 0; j < n; j++){
                a[i][j] = sc.nextInt();
            }
        }
        
        int[] x = new int[n];
        for(int i = 0; i < n; i++){
            x[i] = sc.nextInt(); 
        }
        
        int count = 0;
        
        for(int i = 0; i < m; i++){
            for(int j = 0; j < n; j++){
                if(a[i][j] == x[j]){
                    count++;
                }
                if(count == n){
                    System.out.println(i+1);
                }
            }
            count = 0;
        }
        
    }
}


import java.util.Scanner;

public class Main{
	public static void main(String[] args){
		Scanner sc = new Scanner(System.in);

		int m = sc.nextInt();
		int n = sc.nextInt();

		int a[][] = new int[m][n];
		for(int i = 0; i < m; i++){
			for(int j = 0; j < n; j++){
				a[i][j] = sc.nextInt();
			}
		}

		int x[] = new int[n];
		for(int i = 0; i < n; i++){
			x[i] = sc.nextInt();
		}

		int posOfX = -1;
		for(int i = 0; i < m; i++){
			boolean isX = true;
			for(int j = 0; j < n; j++){
				if(a[i][j] != x[j])	isX = false;
			}
			if(isX){
				posOfX = i+1;
				break;
			}
		}

		System.out.println(posOfX);
	}
}
