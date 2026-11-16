public class QueueQ4 {
    public static void main(String[] args) {
        int[] queue = new int[10];
        int front = 0;
        int rear = -1;

        // Enqueue(10)
        queue[++rear] = 10;
        display(queue, front, rear);

        // Enqueue(20)
        queue[++rear] = 20;
        display(queue, front, rear);

        // Enqueue(30)
        queue[++rear] = 30;
        display(queue, front, rear);

        // Dequeue()
        System.out.println("Dequeued: " + queue[front++]);
        display(queue, front, rear);

        // Enqueue(40)
        queue[++rear] = 40;
        display(queue, front, rear);

        // Dequeue()
        System.out.println("Dequeued: " + queue[front++]);
        display(queue, front, rear);

        System.out.println("Front element: " + queue[front]);
    }

    static void display(int[] queue, int front, int rear) {
        System.out.print("Queue (front to rear): [");
        for (int i = front; i <= rear; i++) {
            System.out.print(queue[i]);
            if (i < rear) {
                System.out.print(", ");
            }
        }
        System.out.println("]");
    }
}
