    #include<iostream>
using namespace std;

void inf();
void ilkom();
void SI();

int main(){
  int code;
  cout<<"Bismillaahirrahmaanirrahiim, Saya Nabila Lailatanzila\n"<<endl;
  cout<<"berjanji akan mengerjakan soal UAS ini dengan sungguh-sungguh dan maksimal dengan usaha sendiri\n"<<endl;
  cout<<"TIDAK melihat pekerjaan orang lain, serta mematuhi peraturan selama ujian\n" <<endl;
  cout<<"Jika saya tidak menepati janji ini, saya akan menanggung risikonya\n"<<endl;
  cout<<"==================================================================================="<<endl;
  cout<<"Masukan kode jurusan!" << endl;
  cin >> code;

  switch(code){
    case 1001:
      inf();
      break;
    case 2002:
      ilkom();
      break;
    case 3003:
      SI();
      break;
  }
}

void inf(){
  system("cls");
  
  int total_mhs;
  cout <<"TEKNIK INFORMATIKA"<<endl;
  cout<<"===================="<<endl;
  cout <<"Masukan jumlah mahasiswa yang akan diinput nilainya :";
  cin >> total_mhs;
  string matkul[4] = {"Dasar Pemrograman","Struktur Data","Algoritma Pemrograman","Rekayasa Perangkat Lunak"};
  string mhs[total_mhs][2];
  int score[total_mhs][5];


  for(int i = 0; i < total_mhs; i++){
    cout <<endl<< "Masukan data mahasiswa ke - " << i+1 << endl;
    cout << "NIM: ";
    cin >> mhs[i][0];
    cout << "Nama :";
    cin >> mhs[i][1];
    cout << endl;

    cout << "Masukan nilai skala 0-100" << endl;
    for(int j = 0; j < 4; j++){
      cout << matkul[j] << ": ";
      cin >> score[i][j];
      }
    cout << endl;
    }

  for(int i = 0; i < total_mhs; i++){
    int hasil = 0;
    for(int j = 0; j < 4; j++){
      hasil += score[i][j];
      score[i][4] = hasil;
    }
  }
  
  cout << endl;
  for(int i = 0; i < total_mhs; i++){
    cout << "Data Mahasiswa ke- "<< i+1 <<":"<< endl;
    cout << "NIM :" << mhs[i][0] << endl;
    cout << "Nama :" << mhs[i][1] << endl;

    for(int j = 0; j<4; j++){
      cout << matkul[j] << " : " << score[i][j] << endl;
    }
    cout << endl<< "Rata Rata Nilai Mahasiswa atas nama "<<mhs[i][1] <<" adalah " <<score[i][4] / 4 << endl;
    cout << endl;
}

}

void SI(){
  system("cls");
  int total_mhs;
  cout<<"SiSTEM INFORMASI"<<endl;
  cout<<"================"<<endl;
  cout << "Masukan jumlah mahasiswa yang akan diinput nilainya :";
  cin >> total_mhs;
  string matkul[4] = {"Rekayasa Sistem Informasi","Struktur Data","Algoritma Pemrograman","Konsep sistem informasi"};
  string mhs[total_mhs][2];
  int score[total_mhs][5];

  for(int i = 0; i < total_mhs; i++){
    cout <<endl<< "Masukan data mahasiswa ke - " << i+1 << endl;
    cout << "NIM: ";
    cin >> mhs[i][0];
    cout << "Nama :";
    cin >> score[i][1];
    cout << endl;

    cout << "Masukan nilai (skala 0-100)" << endl;
    for(int j = 0; j < 4; j++){
      cout << matkul[j] << ": ";
      cin >> score[i][j];
      }
    cout << endl;
    }

  for(int i = 0; i < total_mhs; i++){
    int hasil = 0; 
    for(int j = 0; j < 4; j++){
      hasil += score[i][j];
      score[i][4] = hasil;
    }
  }

  cout << endl;
  for(int i = 0; i < total_mhs; i++){
    cout << "Data Mahasiswa ke- " << i+1 << ":" << endl;
    cout << "NIM :" << mhs[i][0] << endl;
    cout << "Nama :" << mhs[i][1] << endl;

    for(int j = 0; j<4; j++){
      cout << matkul[j] << " : " << score[i][j] << endl;
    }
    cout << endl<< "Rata Rata Nilai Mahasiswa atas nama "<<mhs[i][1] <<" adalah " <<score[i][4] / 4 << endl;
  }
}

void ilkom(){
  system("cls");
  int total_mhs;
  cout<<"ILMU KOMPUTER"<<endl;
  cout<<"============="<<endl;
  cout << "Masukan jumlah mahasiswa yang akan diinput nilainya :";
  cin >> total_mhs;
  string matkul[4] = {"Rekayasa Perangkat Lunak","Jaringan komputer","Sistem Cerdas","Sistem Digital"};
  string mhs[total_mhs][2];
  int score[total_mhs][5];


  cout << endl;
  for(int i = 0; i < total_mhs; i++){
    cout << "Masukan data mahasiswa ke - " << i+1 << endl;
    cout << "NIM: ";
    cin >> mhs[i][0];
    cout << "Nama :";
    cin >> mhs[i][1];
    cout << endl;

    cout << "Masukan nilai skala 0-100" << endl;
    for(int j = 0; j<4; j++){
      cout << matkul[j] << ": ";
      cin >> score[i][j];
      }
    cout << endl;
    }

  for(int i = 0;  i < total_mhs; i++){
    int hasil = 0;
    for(int j = 0; j<4; j++){
      hasil += score[i][j];
      score[i][4] = hasil;
    }
  }

  for(int i = 0; i < total_mhs; i++){
    cout <<endl<< "Data Mahasiswa ke- " << i+1 << ":" << endl;
    cout << "NIM :" << mhs[i][0] << endl;
    cout << "Nama :" << mhs[i][1] << endl;

    for(int j = 0; j<4; j++){
      cout << matkul[j] << " : " << score[i][j] << endl;
    }
     cout << endl<< "Rata Rata Nilai Mahasiswa atas nama "<<mhs[i][1] <<" adalah " <<score[i][4] / 4 << endl;
  }
}
