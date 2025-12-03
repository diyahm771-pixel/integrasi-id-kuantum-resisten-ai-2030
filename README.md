#include <stdio.h>

int main() {
    int pilihan;
    float a, b, hasil;

    printf("=== PROGRAM KALKULATOR ===\n");
    printf("Masukkan bilangan pertama : ");
    scanf("%f", &a);
    printf("Masukkan bilangan kedua   : ");
    scanf("%f", &b);

    printf("\nMenu Operasi:\n");
    printf("1. Penjumlahan\n");
    printf("2. Pengurangan\n");
    printf("3. Perkalian\n");
    printf("4. Pembagian\n");
    printf("Pilih menu (1-4): ");
    scanf("%d", &pilihan);

    switch(pilihan) {
        case 1:
            hasil = a + b;
            printf("Hasil penjumlahan = %.2f\n", hasil);
            break;

        case 2:
            hasil = a - b;
            printf("Hasil pengurangan = %.2f\n", hasil);
            break;

        case 3:
            hasil = a * b;
            printf("Hasil perkalian = %.2f\n", hasil);
            break;

        case 4:
            if (b != 0) {
                hasil = a / b;
                printf("Hasil pembagian = %.2f\n", hasil);
            } else {
                printf("Error: Pembagi tidak boleh nol!\n");
            }
            break;

        default:
            printf("Pilihan tidak valid!\n");
    }

    return 0;
}
