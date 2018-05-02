# Soal Ujian Purwadhika Mobile Development

![Lintang_Purwadhika](https://static.wixstatic.com/media/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png/v1/fill/w_246,h_39,al_c,usm_0.66_1.00_0.01/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png)

**Materi Mobile Dev dapat diakses di [klik sini!](https://github.com/LintangWisesa/Purwadhika-JC04-04_Mobile)**

#
### **Soal 1 - Aplikasi Indeks Massa Tubuh**

Buatlah sebuah aplikasi React Native penghitung **Indeks Massa Tubuh (IMT)**, yang memenuhi spesifikasi berikut:

- Elemen utama aplikasi terdiri atas 2 buah teks input (untuk input _**massa (kg)**_ dan _**tinggi (cm)**_) serta 1 buah button.

- Setelah user memasukkan nilai pada teks input _**massa (kg)**_ dan _**tinggi (cm)**_, kemudian user menekan tombol button (satu kali tekan), maka aplikasi akan menampilkan: _**massa (kg)**_, _**tinggi (m)**_, _**indeks massa tubuh**_ dan _**diagnosis**_ (arti dari nilai IMT).

- Indeks Massa Tubuh dapat dihitung dengan rumus:
  
  >__*IMT = massa(kg) / tinggi(m)^2*__

- Adapun diagnosis berdasarkan nilai IMT adalah sebagai berikut:
  - **IMT < 18.5** artinya berat badan kurang,
  - **IMT 18.5 - 24.9** artinya berat badan ideal,
  - __IMT 25.0 - 29.9__ artinya BB berlebih,
  - **IMT 30.0 - 39.9** artinya BB sangat berlebih,
  - **IMT > 39.9** artinya obesitas.

- Contoh tampilan antarmuka aplikasi yang diharapkan (tidak harus sama persis):

  ![Lintang_App1](https://2.bp.blogspot.com/-cJ0XRmZOoNI/WujSaxugEbI/AAAAAAAAEEU/3Epu_8TeoFgGCEonRUChPKMYe9HK_6jSwCLcBGAs/s1600/soal1.png)

>_**Catatan:**_ *Commit/upload project ini ke akun Github Anda dengan nama repo: **ReactNative-IMT-namaAnda**. Salin App.js aplikasi ini ke dalam format .txt, sertakan link url ke repo Github project ini. Kemudian kirimkan via email ke lintang@purwadhika.com dengan subject email: __ReactNative-IMT-namaAnda__.*

#
### **Soal 2 - GET Zomato API**

Buatlah sebuah aplikasi React Native pencari restaurant, yang memenuhi spesifikasi berikut:

- Elemen utama aplikasi: 1 buah input teks, 1 buah button dan card untuk menampilkan hasil pencarian.

- Elemen input teks digunakan oleh user untuk memasukkan nama menu makanan yang dicari, kemudian aplikasi akan menampilkan daftar restaurant yang menyediakan menu tersebut. Misal: user memasukkan kata _**kebab**_, kemudian usai menekan tombol, aplikasi akan menampilkan daftar restaurant yang memiliki menu _**kebab**_ dalam bentuk card.

- Aplikasi memanfaatkan API dari [Zomato](https://developers.zomato.com/api). API Zomato dapat diakses dengan menggunakan API key sebagai header.
  
  - GET Request URL = https://developers.zomato.com/api/v2.1/search?q=**_namaMenuYangDicari_**.
  
  - Setting Header = key/param: **_user-key_** dan value: _**API key**_.
  
  - Data yang diambil yakni:
    - Nama restaurant (**.data.restaurants.restaurant.name**)
    - Kota restaurant (__.data.restaurants.restaurant.location.city__)
    - Alamat restaurant (__.data.restaurants.restaurant.location.address__)
    - Harga menu rata-rata 2 porsi (__.data.restaurants.restaurant.average_cost_for_two__)
    - Gambar thumbnail (__.data.restaurants.restaurant.thumb__)

  - Data ditampilkan dalam bentuk card, format bebas. Data yang ditampilkan yakni:
    - Nama restaurant 
    - Kota restaurant 
    - Alamat restaurant 
    - Harga menu rata-rata untuk 1 porsi 
    - Gambar thumbnail

  - Proses GET API Zomato dengan setting Header pada Axios, untuk mencari daftar restaurant yang memiliki menu __*kebab*__, dapat dilakukan dengan menggunakan struktur berikut:
    ```javascript
    ...
    var url = 'https://developers.zomato.com/api/v2.1/search?q=kebab';
    
    var config = {
      headers:{'user-key':'d1b8cxxxxxx544f7'}
    };

    axios.get(url, config).then((ambilData)=>{
      this.setState({
        resto: ambilData.data.restaurants,
      })
    })
    ...
    ``` 

  - Adapun proses GET API Zomato dengan setting Header pada Postman, untuk mencari daftar restaurant yang memiliki menu __*kebab*__, adalah sebagai berikut:

    ![Lintang_Get_Zomato](https://3.bp.blogspot.com/-9s6KfiCp3-0/Wuji-Z571YI/AAAAAAAAEEs/3Is7s87qa2s98O8OFUEsVbwFp7FLH0xngCLcBGAs/s1600/soal2a.png)

- Contoh tampilan antarmuka aplikasi yang diharapkan (tidak harus sama persis):

  ![Lintang_App2](https://4.bp.blogspot.com/-KV1W_AYbKq0/WujSbM1WU0I/AAAAAAAAEEY/7VkHIUn3E5AhMTvU3mjzh4B7tn86JM9zwCLcBGAs/s1600/soal2.png)

- Done.

>_**Catatan:**_ *Commit/upload project ini ke akun Github Anda dengan nama repo: **ReactNative-Zomato-namaAnda**. Salin App.js aplikasi ini ke dalam format .txt, sertakan pula link url ke repo Github project ini. Kemudian kirimkan via email ke lintang@purwadhika.com dengan subject email: __ReactNative-Zomato-namaAnda__.*

#
*__#HappyCoding__*
