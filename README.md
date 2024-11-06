void fibonacci(int limit) {
    int a = 0, b = 1, next;
    printf("Fibonacci Series up to %d:\n", limit);

    for (int i = 1; i <= limit; i++) {
        printf("%d ", a);
        next = a + b;
        a = b;
        b = next;
    }
    printf("\n");
}
