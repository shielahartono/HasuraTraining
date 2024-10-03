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




## 3. Analisis Hasil Grafana untuk Hasura 


