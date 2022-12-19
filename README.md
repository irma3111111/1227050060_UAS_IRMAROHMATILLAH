DESKRIPSI
Menampilkan bilangan yang habis dibagi 3, 5 dan 7
Pada program ini kita akan mengecek bilangan yang diinputkan apakah bisa dibagi dengan bilangan 3, 5, 7 atau tidak

SOURCE CODE
#include <iostream>
#include <iomanip>
using namespace std;
int main(){
    
	int arr[100][100], jumlahBaris, jumlahKolom, i, j, baris, kolom;

    cout<<"Input jumlah baris: "; cin>>jumlahBaris;
    cout<<"Input jumlah kolom: "; cin>>jumlahKolom;
    cout << endl;

    for(i = 0; i < jumlahBaris; i++){
        for(j = 0; j < jumlahKolom; j++){
            cout << "Baris " <<i+1<<", kolom "<<j+1<< " = ";
            cin >> arr[i][j];
        }
        cout << endl;
    }

    cout << "Hasil input nilai : " << endl;

    for(i = 0; i < jumlahBaris ; i++){
    for(j = 0; j < jumlahKolom; j++){
        cout << setw(3) << arr[i][j] << " ";
    }
    cout << endl;
    }

    cout << "\nHasil bilangan yang bisa dibagi 3,5,7 : " << endl;

    for(i = 0; i < jumlahBaris ; i++){
    for(j = 0; j < jumlahKolom; j++){
        if(arr[i][j] % 3 == 0 || arr[i][j] % 5 == 0 || arr[i][j] % 7 == 0){
        cout << setw(3) << arr[i][j] << " ";
        }
    }
    cout << endl;
    }

    
    cout << endl;
    return 0;
}


OUTPUT
Input jumlah baris: 2
Input jumlah kolom: 3

Baris 1, kolom 1 = 3
Baris 1, kolom 2 = 4
Baris 1, kolom 3 = 5

Baris 2, kolom 1 = 6
Baris 2, kolom 2 = 7
Baris 2, kolom 3 = 9

Hasil input nilai :
  3   4   5
  6   7   9

Hasil bilangan yang bisa dibagi 3,5,7 :
  3   5
  6   7   9
