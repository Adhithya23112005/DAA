import java.util.ArrayList;
import java.util.List;

public class TextJustification {
    public List<String> fullJustify(String[] words, int maxWidth) {
        List<String> result = new ArrayList<>();
        List<String> currentLine = new ArrayList<>();
        int numOfLetters = 0;

        for (String word : words) {
            if (numOfLetters + word.length() + currentLine.size() > maxWidth) {
                for (int i = 0; i < maxWidth - numOfLetters; i++) {
                    currentLine.set(i % (currentLine.size() - 1 == 0 ? 1 : currentLine.size() - 1), 
                                    currentLine.get(i % (currentLine.size() - 1 == 0 ? 1 : currentLine.size() - 1)) + " ");
                }
                result.add(String.join("", currentLine));
                currentLine.clear();
                numOfLetters = 0;
            }
            currentLine.add(word);
            numOfLetters += word.length();
        }

        StringBuilder lastLine = new StringBuilder(String.join(" ", currentLine));
        while (lastLine.length() < maxWidth) {
            lastLine.append(" ");
        }
        result.add(lastLine.toString());

        return result;
    }

    public static void main(String[] args) {
        TextJustification tj = new TextJustification();
        String[] words = {"This", "is", "an", "example", "of", "text", "justification."};
        int maxWidth = 16;
        List<String> justifiedText = tj.fullJustify(words, maxWidth);
        
        for (String line : justifiedText) {
            System.out.println('"' + line + '"');
        }
    }
}
