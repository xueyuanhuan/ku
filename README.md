#include <stdio.h>
#define ROWS 4
#define COLS 3
int main() {
    int matrix[ROWS][COLS];
    int max_value, max_row = 0, max_col = 0;
    printf("请输入一个4×3矩阵的元素（12个整数）：\n");
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            printf("matrix[%d][%d] = ", i, j);
            scanf_s("%d", &matrix[i][j]);
        }
    }
    printf("\n您输入的矩阵为：\n");
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            printf("%4d", matrix[i][j]);
        }
        printf("\n");
    }
    max_value = matrix[0][0];
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            if (matrix[i][j] > max_value) {
                max_value = matrix[i][j];
                max_row = i;
                max_col = j;
            }
        }
    }
    printf("\n矩阵中最大元素的信息：\n");
    printf("最大值: %d\n", max_value);
    printf("所在位置: 第%d行, 第%d列\n", max_row + 1, max_col + 1);
    return 0;
}
