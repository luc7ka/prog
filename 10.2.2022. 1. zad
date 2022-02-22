#include <stdio.h>
#include <stdlib.h>
#include <time.h>

/* Omoquciti korisniku unos dimenzija kvadratne matrice (2-D polja) m × m, qdje je m neparan i
4 < m ≤ 24. Popuniti matricu parnim pseudo-slucajnim brojevima iz [-19, 25] c Z. Izracunati
aritmetièku sredinu elemenata ispod glavne dijagonale te aritmeticku sredinu elemenata iznad
sporedne dijagonale. Zatim, izracunati i na ekran ispisati apsolutnu vrijednost razlike izracunatih
aritmetickih sredina. */


int main()
{
    int m;

    do{
        scanf("%d", &m);
        if ((m<=4 || m>24) || (m%2!=0)) {
            printf("Pogreska. Pokusajte ponovno!");
        }
    }while ((m<=4 || m>24) || (m%2!=0));

    srand((unsigned) time(NULL));
    int mat[24][24];
    int i,j;

    for (i=0;i<m;i++) {
        for (j=0;j<m;j++) {

            mat[i][j] = -19 + (float)rand() / RAND_MAX * (25 - (-19) -1);
        }
    }

    for (i=0;i<m;i++) {
        for (j=0;j<m;j++) {
            printf(" %d ", mat[i][j]);
        }
        printf("\n");
    }

    float sum=0;
    int sv1;
    int br=0;
    for (i=0;i<m;i++) {
        for (j=0;j<m;j++) {
            if (i>j) {
                printf("%d ", mat[i][j]);
                br++;
                sum = sum + mat[i][j];
            }
        }
    }
    printf("Brojac je %d", br);
    printf("Sum je %d", sum);
    printf("Sv je %f", sv1);

    sv1 = sum / br;
    printf("Srednja vrijednost ispod glavne dijagonale je %f.", sv1);




    return 0;
}
