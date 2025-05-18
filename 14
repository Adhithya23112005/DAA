import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int q = scanner.nextInt(); 
        for (int i = 0; i < q; i++) {
            int n = scanner.nextInt(); 
            int leap = scanner.nextInt();
            int[] game = new int[n];

            for (int j = 0; j < n; j++) {
                game[j] = scanner.nextInt();
            }

           
            System.out.println(canWin(leap, game) ? "YES" : "NO");
        }
        
        scanner.close();
    }

    public static boolean canWin(int leap, int[] game) {
        return canWinHelper(0, leap, game, new boolean[game.length]);
    }

    private static boolean canWinHelper(int index, int leap, int[] game, boolean[] visited) {
       
        if (index >= game.length) {
            return true;
        }
        // If index is out of bounds or cell is blocked or already visited
        if (index < 0 || game[index] == 1 || visited[index]) {
            return false;
        }

        
        visited[index] = true;

       
       
        if (canWinHelper(index + 1, leap, game, visited)) {
            return true;
        }
        
        if (canWinHelper(index + leap, leap, game, visited)) {
            return true;
        }
       
        if (canWinHelper(index - 1, leap, game, visited)) {
            return true;
        }

        
        return false;
    }
}
