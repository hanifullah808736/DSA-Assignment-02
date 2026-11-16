public class StackQ2 {
    public static void main(String[] args) {
        int[] stack = new int[10];
        int top = -1;

        // Push(10)
        stack[++top] = 10;
        display(stack, top);

        // Push(20)
        stack[++top] = 20;
        display(stack, top);

        // Push(30)
        stack[++top] = 30;
        display(stack, top);

        // Pop()
        System.out.println("Popped: " + stack[top--]);
        display(stack, top);

        // Push(40)
        stack[++top] = 40;
        display(stack, top);

        // Pop()
        System.out.println("Popped: " + stack[top--]);
        display(stack, top);

        System.out.println("Final top element: " + stack[top]);
    }

    static void display(int[] stack, int top) {
        System.out.print("Stack (bottom to top): [");
        for (int i = 0; i <= top; i++) {
            System.out.print(stack[i]);
            if (i < top) {
                System.out.print(", ");
            }
        }
        System.out.println("]");
    }
}
