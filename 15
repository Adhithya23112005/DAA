import java.util.*;

public class Solution {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Read number of lines
        int n = scanner.nextInt();
        scanner.nextLine(); // Consume the newline character
        
        // Create a list to store the lines
        List<ArrayList<Integer>> list = new ArrayList<>();
        
        // Read each line
        for (int i = 0; i < n; i++) {
            String line = scanner.nextLine();
            String[] numbers = line.split(" ");
            int count = Integer.parseInt(numbers[0]); // Number of integers on this line
            
            ArrayList<Integer> tempList = new ArrayList<>();
            for (int j = 1; j <= count; j++) {
                tempList.add(Integer.parseInt(numbers[j]));
            }
            list.add(tempList); 
        }
        
        
        int q = scanner.nextInt();
        
       
        for (int i = 0; i < q; i++) {
            int lineIndex = scanner.nextInt() - 1;
            int position = scanner.nextInt() - 1; 
            
            // Check if the line index and position are valid
            if (lineIndex >= 0 && lineIndex < list.size() && position >= 0 && position < list.get(lineIndex).size()) {
                System.out.println(list.get(lineIndex).get(position));
            } else {
                System.out.println("ERROR!");
            }
        }
        
        scanner.close();
    }
}
