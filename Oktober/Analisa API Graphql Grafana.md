# Analisa API Graphql Grafana (Dashboard Hasura HTTP Graphql dan Hasura Health)

## 1. Akses Grafana

        Untuk akses ke grafana HARUS menyalakan VPN
  
        Untuk alamat akses yang digunakan yaitu :
        
```
   1. URL : 10.100.13.8:3000
   2. username: admin
   3. password : password
```


## 2. Melakukan Akses dan Hit melalui Postman

      1. Untuk akses Hasura disini menggunakan Hasura dari Mas Ferdi :

      

```
  1. URL : http://10.100.13.24/console
  2. Password : myadminsecretkey
```




    2. Disini saya melakukan hit dengan method POST menggunakan Postman 

    Berikut untuk Query yang digunakan: 


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


## 3. Analisis Hasil Grafana untuk Hasura 


