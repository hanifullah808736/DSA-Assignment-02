import java.util.Scanner;

public class ArrayStackProgram {
    private final int[] stack;
    private int top = -1;

    public ArrayStackProgram(int capacity) {
        stack = new int[capacity];
    }

    public void push(int value) {
        if (top == stack.length - 1) {
            System.out.println("Stack Overflow: the stack is full.");
            return;
        }

        stack[++top] = value;
        System.out.println(value + " pushed onto the stack.");
    }

    public void pop() {
        if (top == -1) {
            System.out.println("Stack Underflow: the stack is empty.");
            return;
        }

        System.out.println(stack[top--] + " popped from the stack.");
    }

    public void peek() {
        if (top == -1) {
            System.out.println("Stack Underflow: the stack is empty.");
            return;
        }

        System.out.println("Top element: " + stack[top]);
    }

    public void display() {
        if (top == -1) {
            System.out.println("Stack is empty.");
            return;
        }

        System.out.print("Stack (top to bottom): ");
        for (int i = top; i >= 0; i--) {
            System.out.print(stack[i] + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter stack capacity: ");
        int capacity = input.nextInt();

        if (capacity <= 0) {
            System.out.println("Capacity must be greater than zero.");
            input.close();
            return;
        }

        ArrayStackProgram stack = new ArrayStackProgram(capacity);
        int choice;

        do {
            System.out.println("\n1. Push");
            System.out.println("2. Pop");
            System.out.println("3. Peek");
            System.out.println("4. Display");
            System.out.println("0. Exit");
            System.out.print("Choose an operation: ");
            choice = input.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter value to push: ");
                    stack.push(input.nextInt());
                    break;
                case 2:
                    stack.pop();
                    break;
                case 3:
                    stack.peek();
                    break;
                case 4:
                    stack.display();
                    break;
                case 0:
                    System.out.println("Program ended.");
                    break;
                default:
                    System.out.println("Invalid choice. Try again.");
            }
        } while (choice != 0);

        input.close();
    }
}
