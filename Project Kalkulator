#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>

// ------------------------------------------------------------
// 1. Fungsi Hukum Ohm
// ------------------------------------------------------------
void hukumOhm() {
    int pilihan;
    double V, I, R;

    printf("\n--- Kalkulator Hukum Ohm (V = I * R) ---\n");
    printf("Hitung apa?\n");
    printf("1. Tegangan (V)\n");
    printf("2. Arus (I)\n");
    printf("3. Hambatan (R)\n");
    printf("Pilihan: ");
    scanf("%d", &pilihan);

    switch (pilihan) {
        case 1:
            printf("Masukkan Arus (I): ");
            scanf("%lf", &I);
            printf("Masukkan Hambatan (R): ");
            scanf("%lf", &R);
            V = I * R;
            printf("Tegangan (V) = %.4lf Volt\n", V);
            break;

        case 2:
            printf("Masukkan Tegangan (V): ");
            scanf("%lf", &V);
            printf("Masukkan Hambatan (R): ");
            scanf("%lf", &R);
            I = V / R;
            printf("Arus (I) = %.4lf Ampere\n", I);
            break;

        case 3:
            printf("Masukkan Tegangan (V): ");
            scanf("%lf", &V);
            printf("Masukkan Arus (I): ");
            scanf("%lf", &I);
            R = V / I;
            printf("Hambatan (R) = %.4lf Ohm\n", R);
            break;

        default:
            printf("Pilihan tidak valid!\n");
    }
}

// ------------------------------------------------------------
// 2. Kalkulator Daya
// ------------------------------------------------------------
void dayaListrik() {
    double V, I, P;

    printf("\n--- Kalkulator Daya Listrik (P = V * I) ---\n");

    printf("Masukkan Tegangan (V): ");
    scanf("%lf", &V);

    printf("Masukkan Arus (I): ");
    scanf("%lf", &I);

    P = V * I;

    printf("Daya (P) = %.4lf Watt\n", P);
}

// ------------------------------------------------------------
// 3. Resistor Seri
// ------------------------------------------------------------
void resistorSeri() {
    int n;
    double R, total = 0;

    printf("\n--- Kalkulator Resistor Seri ---\n");
    printf("Masukkan jumlah resistor: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        printf("Masukkan nilai Resistor %d (Ohm): ", i);
        scanf("%lf", &R);
        total += R;
    }

    printf("Total Hambatan Seri = %.4lf Ohm\n", total);
}

// ------------------------------------------------------------
// 4. Resistor Paralel
// ------------------------------------------------------------
void resistorParalel() {
    int n;
    double R, sumInv = 0;

    printf("\n--- Kalkulator Resistor Paralel ---\n");
    printf("Masukkan jumlah resistor: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        printf("Masukkan nilai Resistor %d (Ohm): ", i);
        scanf("%lf", &R);
        sumInv += 1.0 / R;
    }

    double total = 1.0 / sumInv;

    printf("Total Hambatan Paralel = %.4lf Ohm\n", total);
}

// ------------------------------------------------------------
// 5. Konversi Desimal → Biner, Oktal, Hex
// ------------------------------------------------------------
void convertDecimal() {
    long long decimal;

    printf("\n--- Konversi dari Desimal ---\n");
    printf("Masukkan bilangan desimal: ");
    scanf("%lld", &decimal);

    printf("Hasil Konversi:\n");

    // Biner
    printf("- Biner : %llb (gunakan printf dengan %llb jika compiler mendukung)\n");

    // Oktal
    printf("- Oktal : %llo\n", decimal);

    // Hexa
    printf("- Heksadesimal : %llX\n", decimal);
}

// ------------------------------------------------------------
// 6. Biner → Desimal
// ------------------------------------------------------------
void binerKeDesimal() {
    char bin[100];
    long long decimal = 0;

    printf("\n--- Konversi Biner ke Desimal ---\n");
    printf("Masukkan bilangan biner: ");
    scanf("%s", bin);

    int len = strlen(bin);

    for (int i = 0; i < len; i++) {
        if (bin[i] != '0' && bin[i] != '1') {
            printf("Input bukan biner!\n");
            return;
        }
        decimal = decimal * 2 + (bin[i] - '0');
    }

    printf("Hasil Desimal: %lld\n", decimal);
}

// ------------------------------------------------------------
// 7. Oktal → Desimal
// ------------------------------------------------------------
void oktalKeDesimal() {
    char oct[100];
    long long decimal = 0;

    printf("\n--- Konversi Oktal ke Desimal ---\n");
    printf("Masukkan bilangan oktal: ");
    scanf("%s", oct);

    int len = strlen(oct);

    for (int i = 0; i < len; i++) {
        if (oct[i] < '0' || oct[i] > '7') {
            printf("Input bukan oktal!\n");
            return;
        }
        decimal = decimal * 8 + (oct[i] - '0');
    }

    printf("Hasil Desimal: %lld\n", decimal);
}

// ------------------------------------------------------------
// 8. Hex → Desimal
// ------------------------------------------------------------
int hexValue(char c) {
    if (isdigit(c)) return c - '0';
    c = toupper(c);
    return c - 'A' + 10;
}

void hexKeDesimal() {
    char hex[100];
    long long decimal = 0;

    printf("\n--- Konversi Heksadesimal ke Desimal ---\n");
    printf("Masukkan bilangan heksadesimal: ");
    scanf("%s", hex);

    int len = strlen(hex);

    for (int i = 0; i < len; i++) {
        if (!isxdigit(hex[i])) {
            printf("Input bukan hex!\n");
            return;
        }
        decimal = decimal * 16 + hexValue(hex[i]);
    }

    printf("Hasil Desimal: %lld\n", decimal);
}

// ------------------------------------------------------------
// MENU UTAMA
// ------------------------------------------------------------
int main() {
    int pilihan;

    do {
        printf("\n==============================================\n");
        printf(" TOOLKIT LENGKAP ASISTEN LABORATORIUM ELEKTRO\n");
        printf("==============================================\n");
        printf(" 1. Kalkulator Hukum Ohm\n");
        printf(" 2. Kalkulator Daya Listrik\n");
        printf(" 3. Kalkulator Resistor Seri\n");
        printf(" 4. Kalkulator Resistor Paralel\n");
        printf(" 5. Desimal -> Biner/Oktal/Heksadesimal\n");
        printf(" 6. Biner -> Desimal\n");
        printf(" 7. Oktal -> Desimal\n");
        printf(" 8. Heksadesimal -> Desimal\n");
        printf(" 9. Keluar\n");
        printf("----------------------------------------------\n");

        printf("Masukkan pilihan Anda: ");
        scanf("%d", &pilihan);

        switch (pilihan) {
            case 1: hukumOhm(); break;
            case 2: dayaListrik(); break;
            case 3: resistorSeri(); break;
            case 4: resistorParalel(); break;
            case 5: convertDecimal(); break;
            case 6: binerKeDesimal(); break;
            case 7: oktalKeDesimal(); break;
            case 8: hexKeDesimal(); break;
            case 9: printf("Terima kasih telah menggunakan toolkit!\n"); break;
            default: printf("Pilihan tidak valid!\n");
        }

        printf("\nTekan Enter untuk melanjutkan...");
        getchar();
        getchar();

        system("cls"); // gunakan "clear" untuk Linux

    } while (pilihan != 9);

    return 0;
}
