public class GreaterThanPrevAvg {
    public static int countGreater(int[] arr) {
        int count = 0, sum = arr[0];
        for (int i = 1; i < arr.length; i++) {
            double avg = (double) sum / i;
            if (arr[i] > avg) count++;
            sum += arr[i];
        }
        return count;
    }

    public static void main(String[] args) {
        int[] arr = {2, 4, 6, 8, 10};
        System.out.println(countGreater(arr)); 
    }
}
