import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

       
        int n = scanner.nextInt();
        List<Integer> list = new ArrayList<>();

       
        for (int i = 0; i < n; i++) {
            list.add(scanner.nextInt());
        }

        
        int q = scanner.nextInt();
        scanner.nextLine(); // Consume the newline

       
        for (int i = 0; i < q; i++) {
            String operation = scanner.nextLine();
            if (operation.equals("Insert")) {
                String[] parts = scanner.nextLine().split(" ");
                int index = Integer.parseInt(parts[0]);
                int value = Integer.parseInt(parts[1]);
                list.add(index, value); 
            } else if (operation.equals("Delete")) {
                int index = Integer.parseInt(scanner.nextLine());
                if (index >= 0 && index < list.size()) {
                    list.remove(index); 
                }
            }
        }

       
        for (int i = 0; i < list.size(); i++) {
            System.out.print(list.get(i));
            if (i < list.size() - 1) {
                System.out.print(" "); 
            }
        }
        scanner.close();
    }
}
