void xPowerX(int limit) {
    printf("X^X Series up to %d:\n", limit);
    for (int i = 1; i <= limit; i++) {
        printf("%.0f ", pow(i, i));
    }
    printf("\n");
}
