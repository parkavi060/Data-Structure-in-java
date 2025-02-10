import java.util.*;

public class Main {
    
    // Partition function for QuickSort
    public static int partition(int a[], int lb, int ub) {
        int mid = lb + (ub - lb) / 2;
        int pivot = a[mid];
        int start = lb;
        int end = ub;

        while (start <= end) {
            while (a[start] < pivot) start++; // Move start right if value is smaller
            while (a[end] > pivot) end--; // Move end left if value is greater
            
            if (start <= end) { // Swap elements when needed
                int temp = a[start];
                a[start] = a[end];
                a[end] = temp;
                start++;
                end--;
            }
        }
        return start; // Return partition index
    }

    // QuickSort Function
    public static void quicksort(int a[], int lb, int ub) {
        if (lb < ub) {
            int loc = partition(a, lb, ub);
            quicksort(a, lb, loc - 1);
            quicksort(a, loc, ub);
        }
    }

    // Main Function
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        // Display Instructions
        System.out.println("💡 QuickSort Program in Java 💡");
        System.out.println("--------------------------------");
        System.out.println("➡ Step 1: Enter the size of the array.");
        System.out.println("➡ Step 2: Enter the elements one by one.");
        System.out.println("➡ Step 3: The program will sort the array using QuickSort.");
        System.out.println("➡ Step 4: The sorted array will be displayed.\n");

        // Taking input from the user
        System.out.print("Enter the size of an array: ");
        int size = scan.nextInt();
        int a[] = new int[size];

        System.out.println("Enter the elements to sort:");
        for (int i = 0; i < size; i++) {
            a[i] = scan.nextInt();
        }

        // Sorting the array
        quicksort(a, 0, size - 1);

        // Display sorted array
        System.out.println("\n✅ Array after QuickSort:");
        for (int i = 0; i < size; i++) {
            System.out.print(a[i] + " ");
        }
        System.out.println("\n");

        // Closing scanner
        scan.close();
    }
}
