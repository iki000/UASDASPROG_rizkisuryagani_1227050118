# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemrograman
<br> Nama		: Rizki Surya Gani
<br>NIM		:1227050118	
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum

 Pembuatan program kolom,baris menggunakan array 2 dimensi dan menampilkan bilangan yang habis dibagi 3,5,7
Pengertian Arra
Array adalah sebuah variabel yang mampu menampung banyak value(data)yang bertipe data sama sesuai dengan inisiasi tipe data pada array yang nantinya kita buat setiap value (data) pada array   

akan disimpan pada memori yang berbeda beda walaupun satu variabel yang diinisialisasi
## Source Code

#include <iostream>
#include <iomanip>
 
using namespace std;
 
int main()
{
  cout << "##  Program C++ Input Matriks 2 Dimensi ##" << endl;
  cout << "==========================================" << endl;
  cout << endl;
 
  int matriks[100][100], tranfous[100][100];
  int jum_baris, jum_kolom, i, j, n, m;
 
  cout << "Input jumlah baris matriks: ";
  cin >> jum_baris;
 
  cout << "Input jumlah kolom matriks: ";
  cin >> jum_kolom;
  cout << endl;
 
  // proses input array
  for(i = 0; i < jum_baris ; i++){
    for(j = 0; j < jum_kolom; j++){
      cout << "Baris " <<i+1<<", kolom "<<j+1<< " = ";
      cin >> matriks[i][j];
    }
    cout << endl;
  }
 
  cout << "Hasil matriks: " << endl;
 
  // menampilkan array
  for(i = 0; i < jum_baris ; i++){
    for(j = 0; j < jum_kolom; j++){
      cout << setw(3) << matriks[i][j] << " ";
    }
    cout << endl;
  }
  for(i = 0; i < jum_baris ; i++){
    for(j = 0; j < jum_kolom; j++){
      tranfous [j][i]=matriks[i][j];
    }
    cout << endl;
  }
  for(i = 0; i < jum_baris ; i++){
    for(j = 0; j < jum_kolom; j++){
      cout << tranfous [j][i];
    }
    cout << endl;
  }
  
 cout << "No.2 Menampilkan bilangan yang habis dibagi 3, 5 dan 7" << endl;
	cout << "==============================================================="<<endl;
	cout << "Masukkan jumlah baris matriks: ";
	cin >> m;
	cout << "Masukkan jumlah kolom matriks: ";
	cin >> n;
	
	cout << "Masukkan Nilai-Nilai\n";
	for (int i = 0; i < m; i++)
	{
    	for (int j = 0; j < n; j++)
		{
    		cout <<"("<<i+1<<","<<j+1<<") : ";
			cin  >> matriks[i][j];
		}
	}
	cout << endl;
	
	bool cek = true;
	cout << "Nilai yang bisa dibagi 3, 5, 7 yaitu :";
	for (int i = 0; i < m; i++)
	{
		for (int j = 0; j < n; j++)
		{
			if (matriks[i][j]%3==0 && matriks[i][j]%5==0 && matriks[i][j]%7==0)
			{
				cout << " " << matriks[i][j];
				cout << endl;
				cek = false;
			}
		}
	}
	if (cek)
	{
		cout << " Maaf nilai yang anda input tidak dapat dibagi 3, 5 dan 7" <<endl;
	}
	
  return 0;
}
## Output
##  Program C++ Input Matriks 2 Dimensi ##
==========================================

Input jumlah baris matriks: 2
Input jumlah kolom matriks: 2

Baris 1, kolom 1 = 2
Baris 1, kolom 2 = 3

Baris 2, kolom 1 = 4
Baris 2, kolom 2 = 5

Hasil matriks:
  2   3
  4   5


23
45
No.2 Menampilkan bilangan yang habis dibagi 3, 5 dan 7
===============================================================
Masukkan jumlah baris matriks: 2
Masukkan jumlah kolom matriks: 2
Masukkan Nilai-Nilai
(1,1) : 22
(1,2) : 35
(2,1) : 210
(2,2) : 105

Nilai yang bisa dibagi 3, 5, 7 yaitu : 210
 105

[Process completed - press Enter]
