import java.util.Scanner;

public class ArrayQueueProgram {
    private final int[] queue;
    private int front = 0;
    private int rear = -1;
    private int size = 0;

    public ArrayQueueProgram(int capacity) {
        queue = new int[capacity];
    }

    public void enqueue(int value) {
        if (size == queue.length) {
            System.out.println("Queue Overflow: the queue is full.");
            return;
        }

        rear = (rear + 1) % queue.length;
        queue[rear] = value;
        size++;
        System.out.println(value + " enqueued.");
    }

    public void dequeue() {
        if (size == 0) {
            System.out.println("Queue Underflow: the queue is empty.");
            return;
        }

        System.out.println(queue[front] + " dequeued.");
        front = (front + 1) % queue.length;
        size--;

        if (size == 0) {
            front = 0;
            rear = -1;
        }
    }

    public void showFront() {
        if (size == 0) {
            System.out.println("Queue Underflow: the queue is empty.");
            return;
        }

        System.out.println("Front element: " + queue[front]);
    }

    public void display() {
        if (size == 0) {
            System.out.println("Queue is empty.");
            return;
        }

        System.out.print("Queue (front to rear): ");
        for (int i = 0; i < size; i++) {
            System.out.print(queue[(front + i) % queue.length] + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter queue capacity: ");
        int capacity = input.nextInt();

        if (capacity <= 0) {
            System.out.println("Capacity must be greater than zero.");
            input.close();
            return;
        }

        ArrayQueueProgram queue = new ArrayQueueProgram(capacity);
        int choice;

        do {
            System.out.println("\n1. Enqueue");
            System.out.println("2. Dequeue");
            System.out.println("3. Front");
            System.out.println("4. Display");
            System.out.println("0. Exit");
            System.out.print("Choose an operation: ");
            choice = input.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter value to enqueue: ");
                    queue.enqueue(input.nextInt());
                    break;
                case 2:
                    queue.dequeue();
                    break;
                case 3:
                    queue.showFront();
                    break;
                case 4:
                    queue.display();
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
