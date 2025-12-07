#include <iostream>
using namespace std;

int main() {
    float angka1, angka2, hasil;
    char operasi;
    int ulang = 1;

    while (ulang == 1) {
        cout << "\n=== KALKULATOR SEDERHANA ===\n";

        cout << "Masukkan angka pertama : ";
        cin >> angka1;

        cout << "Masukkan operator (+, -, *, /) : ";
        cin >> operasi;

        cout << "Masukkan angka kedua   : ";
        cin >> angka2;

        switch (operasi) {
            case '+':
                hasil = angka1 + angka2;
                cout << "Hasil: " << hasil << endl;
                break;

            case '-':
                hasil = angka1 - angka2;
                cout << "Hasil: " << hasil << endl;
                break;

            case '*':
                hasil = angka1 * angka2;
                cout << "Hasil: " << hasil << endl;
                break;

            case '/':
                if (angka2 != 0) {
                    hasil = angka1 / angka2;
                    cout << "Hasil: " << hasil << endl;
                } else {
                    cout << "Error: Tidak bisa membagi dengan nol!\n";
                }
                break;

            default:
                cout << "Operator tidak valid!\n";
        }

        cout << "\nHitung lagi? (1 = ya, 0 = tidak): ";
        cin >> ulang;
    }

    cout << "Program selesai.\n";
    return 0;
}
