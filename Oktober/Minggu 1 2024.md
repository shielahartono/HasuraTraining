# Postman Secret Metrics

Penjelasan terkait hasil dari koneksi postman ke port metrics hasura

* hasura_action_request_bytes_total Total size of HTTP request bodies sent via actions (experimental)

  adalah ukuran total dari semua body permintaan HTTP yang dikirim melalui actions dalam Hasura. "Actions" dalam Hasura memungkinkan Anda untuk memperluas logika GraphQL dengan API eksternal atau logika kustom, dan metrik ini mengukur total jumlah data (dalam byte) yang dikirimkan dalam bentuk permintaan HTTP selama penggunaan actions. Penggunaan kata experimental berarti bahwa fitur ini masih dalam status pengembangan

* hasura_action_request_bytes_total counter

  berfungsi untuk mengukur atau menghitung sesuatu yang terus bertambah atau meningkat, seperti jumlah permintaan atau data yang dikirim

* hasura_action_request_bytes_total 0.0

  berarti belum ada data yang dikirim karena masih memiliki jumlah yaitu 0.0 byte

* hasura_active_subscription_pollers Current active number of subscription pollers running

  artinya jumlah saat ini dari subscription pollers yang aktif dan berjalan di Hasura

  Subscription pollers adalah komponen yang memantau perubahan data secara real-time untuk subscriptions (kueri berlangganan) yang dijalankan oleh pengguna


*

