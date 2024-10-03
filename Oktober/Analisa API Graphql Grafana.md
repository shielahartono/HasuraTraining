# 2. Analisa API Graphql Grafana (Dashboard Hasura HTTP Graphql dan Hasura Health)

## 1. Akses Grafana


        
* URL : 10.100.13.8:3000
  
* username: admin
  
* password : password

Gunakan Alamat diatas untuk melakukan akses ke Grafana, dan HARUS mengaktifkan VPN


## 2. Melakukan Akses dan Hit melalui Postman

```
1. URL : http://10.100.13.24/console
2. Password : myadminsecretkey
```

Gunakan alamat diatas untuk mengakses Hasura milik Mas Ferdi 


```
query MyQuery {
  TABEL1 {
    id
    isi1
    isi2
    isi3
  }
}
```
Query diatas merupakan query yang saya gunakan untuk melakukan hit dengan method POST 

![image](https://github.com/user-attachments/assets/eaed9544-0ae5-433d-b13d-ac648e3d3098)


Berikut untuk hasil dari postman :

```
{
    "data": {
        "TABEL1": [
            {
                "id": 1,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 2,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 3,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 4,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 5,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 6,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 7,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 8,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 9,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 10,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 11,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 12,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 13,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 14,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 15,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 16,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 17,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 18,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            },
            {
                "id": 19,
                "isi1": "abc",
                "isi2": "abc",
                "isi3": "abc"
            }
        ]
    }
}

```


## 3. Analisis Hasil Grafana untuk Hasura HTTP Graphql

![image](https://github.com/user-attachments/assets/59a688e8-c00a-48e7-a247-d832d8d298cc)
        
Hasil yang saya ambil disini merupakan hasil 3 jam sebelumnya pada tanggal 3 Oktober 2024


Pada hasil gambar diatas menampilkan data bahwa :

        * Total Queries (Jumlah Query): Sebanyak 70 query telah dilakukan pada Services ini.

        * Query Latency (P95): Latensi atau waktu tunggu untuk query berada pada 26,2 milidetik. 
          Untuk P95 artinya 95% dari query selesai dalam waktu kurang dari atau sama dengan 26,2 ms,               
          yang menunjukkan bahwa performa cukup baik.

