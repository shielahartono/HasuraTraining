# Postman Secret Metrics

## Penjelasan terkait hasil dari koneksi postman ke port metrics hasura

```
# HELP hasura_action_request_bytes_total Total size of HTTP request bodies sent via actions (experimental)
# TYPE hasura_action_request_bytes_total counter
hasura_action_request_bytes_total 0.0
```
* hasura_action_request_bytes_total Total size of HTTP request bodies sent via actions (experimental)

  adalah ukuran total dari semua body permintaan HTTP yang dikirim melalui actions dalam Hasura. "Actions" dalam Hasura memungkinkan Anda untuk memperluas logika    GraphQL dengan API eksternal atau logika kustom, dan metrik ini mengukur total jumlah data (dalam byte) yang dikirimkan dalam bentuk permintaan HTTP selama        penggunaan actions. Penggunaan kata experimental berarti bahwa fitur ini masih dalam status pengembangan

* hasura_action_request_bytes_total counter

  berfungsi untuk mengukur atau menghitung sesuatu yang terus bertambah atau meningkat, seperti jumlah permintaan atau data yang dikirim
  
```

# HELP hasura_action_response_bytes_total Total size of HTTP response bodies received via actions (experimental)
# TYPE hasura_action_response_bytes_total counter
hasura_action_response_bytes_total 0.0
```
* hasura_action_request_bytes_total 0.0

  berarti belum ada data yang dikirim karena masih memiliki jumlah yaitu 0.0 byte


```
# HELP hasura_active_subscription_pollers Current active number of subscription pollers running
# TYPE hasura_active_subscription_pollers gauge
hasura_active_subscription_pollers{subscription_kind="live-query"} 0.0
hasura_active_subscription_pollers{subscription_kind="streaming"} 0.0

```
* hasura_active_subscription_pollers Current active number of subscription pollers running

  artinya jumlah saat ini dari subscription pollers yang aktif dan berjalan di Hasura

  Subscription pollers adalah komponen yang memantau perubahan data secara real-time untuk subscriptions (kueri berlangganan) yang dijalankan oleh pengguna


* hasura_active_subscription_pollers gauge

  metriks ini berguna untuk menunjukan nilai naik turun dari subsciprion pollers yang sedang berjalan secara real time.


* hasura_active_subscription_pollers{subscription_kind="live-query"} 0.0

  metriks ini berarti menunjukkan jumlah poller yang aktif dari jenis berlangganan yaitu "live-query" yang berguna memantau data secara real time, dan untuk hasil   nilai tersebut menunjukkan 0.0 bahwa tidak ada live-query yang sedang berjalan

```

# HELP hasura_event_fetch_time_per_batch_seconds Latency of fetching a batch of events from the database
# TYPE hasura_event_fetch_time_per_batch_seconds histogram
hasura_event_fetch_time_per_batch_seconds_bucket{le="1.0e-4"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="3.0e-4"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="1.0e-3"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="3.0e-3"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="1.0e-2"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="3.0e-2"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="0.1"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="0.3"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="1.0"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="3.0"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="10.0"} 0
hasura_event_fetch_time_per_batch_seconds_bucket{le="+Inf"} 0
hasura_event_fetch_time_per_batch_seconds_sum 0.0
hasura_event_fetch_time_per_batch_seconds_count 0

```
* hasura_event_fetch_time_per_batch_seconds histogram

  metriks ini untuk memantau seberapa cepat Hasura mengambil batch event dari database dan memetakan distribusi latensi pengambilan tersebut dalam berbagai          interval waktu


  1.hasura_event_fetch_time_per_batch_seconds_bucket{le="1.0e-4"} 0
  
      metriks diatas memiliki arti bahwa jumlah event yang diambil dalam waktu kurang dari atau sama dengan 0.0001 detik (1.0e-4) memiliki nilai 0
  
  2.hasura_event_fetch_time_per_batch_seconds_bucket{le="3.0e-4"} 0
  
      metriks diatas memiliki arti bahwa jumlah event yang diambil dalam waktu kurang dari atau sama dengan 0.0003 detik (3.0e-4) memiliki nilai 0


```
# HELP hasura_event_trigger_http_workers Current number of active event trigger HTTP workers
# TYPE hasura_event_trigger_http_workers gauge
hasura_event_trigger_http_workers 0.0
```
* hasura_event_trigger_http_workers 0.0
  
  yang berarti tidak ada pekerja HTTP yang aktif saat ini untuk memproses event trigger. Tidak ada event yang sedang diproses melalui HTTP worker pada saat metrik   ini dicatat.

```
# HELP hasura_event_trigger_request_bytes_total Total size of HTTP request bodies sent via event triggers (experimental)
# TYPE hasura_event_trigger_request_bytes_total counter
hasura_event_trigger_request_bytes_total 0.0
```

* hasura_event_trigger_request_bytes_total 0.0

  berfungsi untuk memantau berapa banyak data yang telah dikirim dalam bentuk permintaan saat event trigger.Untuk nilai 0.0 berarti tidak ada data yang telah        terkirim dalam bentuk request.

```
# HELP hasura_event_trigger_response_bytes_total Total size of HTTP response bodies received via event triggers (experimental)
# TYPE hasura_event_trigger_response_bytes_total counter
hasura_event_trigger_response_bytes_total 0.0
```
* hasura_event_trigger_response_bytes_total 0.0

  bertujuan untuk memantau seberapa banyak data yang diterima sebagai respons setelah permintaan event trigger dilakukan.Untuk nilai 0.0 berarti tidak ada data      yang diterima dalam bentuk respons HTTP melalui event triggers

```

# HELP hasura_events_fetched_per_batch Number of events fetched in a batch
# TYPE hasura_events_fetched_per_batch gauge
hasura_events_fetched_per_batch 0.0
```

* hasura_events_fetched_per_batch 0.0

  digunakan untuk memantau seberapa banyak event yang berhasil diambil dari sumber data dalam satu kali pengambilan atau proses.Untuk nilai 0.0 berarti tidak ada    event yang diambil dalam batch tersebut pada saat metrik ini dicatat.

  metrik ini memberikan informasi tentang efisiensi dan volume event yang diproses dalam sistem.



```
# HELP hasura_graphql_execution_time_seconds Execution time of successful GraphQL requests (excluding subscriptions)
# TYPE hasura_graphql_execution_time_seconds histogram
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="1.0e-2"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="3.0e-2"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="0.1"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="0.3"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="1.0"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="3.0"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="10.0"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="+Inf"} 0
hasura_graphql_execution_time_seconds_sum{operation_type="mutation"} 0.0
hasura_graphql_execution_time_seconds_count{operation_type="mutation"} 0
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="1.0e-2"} 1
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="3.0e-2"} 1
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="0.1"} 1
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="0.3"} 1
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="1.0"} 1
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="3.0"} 1
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="10.0"} 1
hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="+Inf"} 1
hasura_graphql_execution_time_seconds_sum{operation_type="query"} 1.753502e-3
hasura_graphql_execution_time_seconds_count{operation_type="query"} 1
```
* hasura_graphql_execution_time_seconds
  
  metriks ini merupakan metrik histogram yang mencatat waktu eksekusi dari permintaan GraphQL (dalam detik). Metrik ini membantu untuk memantau performa eksekusi    query dan mutation di Hasura.


    1. hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="1.0e-2"} 0
        metriks ini berarti bahwa tidak ada permintaan mutation yang diselesaikan dalam waktu kurang dari atau sama dengan 0.01 detik (10 milidetik).


    2. hasura_graphql_execution_time_seconds_bucket{operation_type="mutation",le="3.0e-2"} 0
        metriks ini menunjukan atau memiliki arti bahwa tidak ada permintaan mutation yang diselesaikan dalam waktu kurang dari atau sama dengan 0.03 detik (30            milidetik)


* hasura_graphql_execution_time_seconds_sum{operation_type="mutation"} 0.0
  
  metriks ini berguna untuk menunjukan total waktu eksekusi untuk semua mutation adalah 0 detik.


* hasura_graphql_execution_time_seconds_count{operation_type="mutation"} 0
  
  metriks ini berguna untuk menunjukan jumlah total mutation yang dieksekusi adalah 0.


    1. hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="1.0e-2"} 1
        metriks ini berarti bahwa 1 query telah dieksekusi dengan waktu eksekusi kurang dari atau sama dengan 0.01 detik (10 milidetik).


    2. hasura_graphql_execution_time_seconds_bucket{operation_type="query",le="3.0e-2"} 1
        metriks ini berarti bahwa 1 query yang sama juga selesai dalam waktu kurang dari atau sama dengan 0.03 detik (30 milidetik).


* hasura_graphql_execution_time_seconds_sum{operation_type="query"} 1.753502e-3
  
  metriks ini berarti untuk total waktu eksekusi untuk semua query yang diproses adalah sekitar 1.753502 milidetik


* hasura_graphql_execution_time_seconds_count{operation_type="query"} 1
  
  metriks ini berarti bahwa hanya terdapat satu permintaan query dalam satu periode pengukuran.



```
# HELP hasura_graphql_requests_total Number of GraphQL requests received (excluding subscriptions)
# TYPE hasura_graphql_requests_total counter
hasura_graphql_requests_total{response_status="success",operation_type="query",parameterized_query_hash="7116865cef017c3b09e5c9271b0e182a6dcf4c01"} 1.0
```
*hasura_graphql_requests_total{response_status="success",operation_type="query",parameterized_query_hash="7116865cef017c3b09e5c9271b0e182a6dcf4c01"} 1.0

  metriks ini berguna untuk melakukan mengambil data request secara total untuk respons status dengan nilai sukses dan juga operation type dengan nilai query. Dan   memeberikan parameter hash untuk identifikasi query yang dijalankan. Dan pada metriks ini terdapat 1 permintaan query yang berhasil di jalankan.

```
# HELP hasura_http_connections Current number of active HTTP connections (excluding WebSocket connections)
# TYPE hasura_http_connections gauge
hasura_http_connections 1.0
```

*hasura_http_connections 1.0

  metriks ini berguna untuk menunjukkan jumlah koneksi HTTP aktif yang sedang digunakan oleh Hasura. Dan pada metriks ini terdapat 1 koneksi aktif yang dibuka       oleh Hasura


```
# HELP hasura_http_request_bytes_total Total size of HTTP request bodies received via the HTTP server
# TYPE hasura_http_request_bytes_total counter
hasura_http_request_bytes_total 1968.0
```

* hasura_http_request_bytes_total 1968.0
  
  metriks ini berguna untuk menunjukkan total ukuran dari semua body permintaan HTTP yang diterima oleh Hasura. Pada nilai ini menunjukkan 1968 byte.


```
# HELP hasura_http_response_bytes_total Total size of HTTP response bodies sent via the HTTP server
# TYPE hasura_http_response_bytes_total counter
hasura_http_response_bytes_total 9051.0
```
* hasura_http_response_bytes_total 9051.0
  
  metriks ini berguna untuk menunjukkan total ukuran dari semua body respons HTTP yang dikirim oleh Hasura. Pada metriks ini menunjukkan hasil 9051 byte.

```
# HELP hasura_metadata_resource_version Current metadata resource version
# TYPE hasura_metadata_resource_version gauge
hasura_metadata_resource_version 22.0
```
* hasura_metadata_resource_version 22.0
  
  metriks ini berguna untuk menunjukkan versi dari metadata yang digunakan oleh Hasura. Saat ini menggunakan versi 22.

```
# HELP hasura_oneoff_events_invocation_total Total number of one-off events invoked
# TYPE hasura_oneoff_events_invocation_total counter
hasura_oneoff_events_invocation_total{status="failed"} 0.0
hasura_oneoff_events_invocation_total{status="success"} 0.0
```
* hasura_oneoff_events_invocation_total{status="failed"} 0.0

  metriks ini menunjukkan jumlah total invokasi (panggilan) untuk one-off events yang gagal.

* hasura_oneoff_events_invocation_total{status="success"} 0.0

  metriks ini menunjukkan jumlah total invokasi (panggilan) untuk one-off events yang berhasil.



```
# HELP hasura_oneoff_events_processed_total Total number of one-off events processed
# TYPE hasura_oneoff_events_processed_total counter
hasura_oneoff_events_processed_total{status="failed"} 0.0
hasura_oneoff_events_processed_total{status="success"} 0.0
```

* hasura_oneoff_events_processed_total{status="failed"} 0.0

  metriks ini menunjukkan jumlah total one-off events yang telah diproses dan berstatus gagal

* hasura_oneoff_events_processed_total{status="success"} 0.0

  metriks ini menunjukkan jumlah total one-off events yang telah diproses dan berstatus success


```
# HELP hasura_otel_dropped_logs Total number of log lines dropped due to high log volume
# TYPE hasura_otel_dropped_logs counter
hasura_otel_dropped_logs{reason="buffer_full"} 0.0
hasura_otel_dropped_logs{reason="send_failed"} 0.0
```

* hasura_otel_dropped_logs{reason="buffer_full"} 0.0

  metriks ini berguna untuk menunjukkan jumlah log yang dibuang oleh sistem observasi Hasura karena buffer yang penuh. Untuk nilai didapatkan yaitu 0 berarti        tidak ada.

* hasura_otel_dropped_logs{reason="send_failed"} 0.0

  metriks ini berguna untuk menunjukkan jumlah log yang dibuang oleh sistem observasi Hasura karena kegagalan pengiriman.


```
# HELP hasura_otel_dropped_spans Total number of trace spans dropped due to high trace volume
# TYPE hasura_otel_dropped_spans counter
hasura_otel_dropped_spans{reason="buffer_full"} 0.0
hasura_otel_dropped_spans{reason="send_failed"} 0.0
```

* hasura_otel_dropped_spans{reason="buffer_full"} 0.0

  metriks ini berguna untuk menunjukkan jumlah "spans" yang dibuang oleh sistem observasi Hasura karena buffer yang penuh.

* hasura_otel_dropped_spans{reason="send_failed"} 0.0

  metriks ini berguna untuk memberikan informasi tentang jumlah spans yang tidak berhasil dikirim oleh sistem observasi Hasura.


```
# HELP hasura_otel_sent_logs Total number of successfully exported log lines
# TYPE hasura_otel_sent_logs counter
hasura_otel_sent_logs 0.0
```
*hasura_otel_sent_logs 0.0

  metriks ini memberikan informasi tentang jumlah log yang berhasil dikirim oleh sistem observasi Hasura.


```
# HELP hasura_otel_sent_spans Total number of successfully exported trace spans
# TYPE hasura_otel_sent_spans counter
hasura_otel_sent_spans 0.0
```
* hasura_otel_sent_spans 0.0

  metriks ini memberikan informasi tentang jumlah "span" yang berhasil dikirim oleh sistem observasi Hasura.

```
# HELP hasura_postgres_connection_init_time Time taken (in seconds) to establish and initialise a new PostgreSQL connection
# TYPE hasura_postgres_connection_init_time histogram
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-6",role="primary"} 0
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-4",role="primary"} 0
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-2",role="primary"} 0
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="0.1",role="primary"} 1
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="0.3",role="primary"} 1
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0",role="primary"} 1
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="3.0",role="primary"} 1
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="10.0",role="primary"} 1
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="30.0",role="primary"} 1
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="100.0",role="primary"} 1
hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="+Inf",role="primary"} 1
hasura_postgres_connection_init_time_sum{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1.5990853e-2
hasura_postgres_connection_init_time_count{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1
```
*  hasura_postgres_connection_init_time histogram

    metriks ini berguna untuk membuat histogram yang mengukur waktu yang diperlukan untuk menginisialisasi koneksi ke basis data PostgreSQL di Hasura.

      1. hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-6",role="primary"} 0

          berarti menunjukkan bahwa tidak ada koneksi yang berhasil diinisialisasi dalam waktu kurang dari atau sama dengan 1.0×10−61.0×10 −6 detik (atau 1                  mikrodetik) untuk database yang terhubung.
         
      2.hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-4",role="primary"} 0

          berarti menunjukkan bahwa tidak ada koneksi ke database yang diinisialisasi dalam waktu kurang dari atau sama dengan 1.0×10−41.0×10 −4 detik (atau 100             mikrodetik) untuk database yang terhubung.
   
      3.hasura_postgres_connection_init_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-2",role="primary"} 0

          berarti tidak ada koneksi ke database yang berhasil diinisialisasi dalam waktu kurang dari atau sama dengan 1.0×10−21.0×10 −2 detik (atau 10 milidetik)            untuk database terhubung. 
         
* hasura_postgres_connection_init_time_sum{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1.5990853e-2

  metriks ini memberikan informasi tentang total waktu inisialisasi koneksi ke database untuk koneksi dengan role primary.

* hasura_postgres_connection_init_time_count{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1

  metriks ini memberikan informasi tentang jumlah koneksi yang telah diinisialisasi ke database PostgreSQL melalui Hasura


```
# HELP hasura_postgres_connections Current number of active PostgreSQL connections
# TYPE hasura_postgres_connections gauge
hasura_postgres_connections{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 0.0
```
* hasura_postgres_connections{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 0.0

  metriks ini menunjukkan


```
# HELP hasura_postgres_max_connections Maximum number of PostgreSQL connections set for this project on the current multitenant worker
# TYPE hasura_postgres_max_connections gauge
hasura_postgres_max_connections{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 50.0
```

* hasura_postgres_max_connections{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 50.0

  metriks ini berarti atau menujukkan


```
# HELP hasura_postgres_pool_wait_time Time taken (in seconds) to acquire a connection from the pool
# TYPE hasura_postgres_pool_wait_time histogram
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-6",role="primary"} 0
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-4",role="primary"} 0
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-2",role="primary"} 0
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="0.1",role="primary"} 1
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="0.3",role="primary"} 1
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0",role="primary"} 1
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="3.0",role="primary"} 1
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="10.0",role="primary"} 1
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="30.0",role="primary"} 1
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="100.0",role="primary"} 1
hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="+Inf",role="primary"} 1
hasura_postgres_pool_wait_time_sum{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1.6099813e-2
hasura_postgres_pool_wait_time_count{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1
```
*  hasura_postgres_pool_wait_time histogram

   metriks ini

     1. hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="1.0e-2",role="primary"} 0
        
        metriks ini
        
     2.hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="0.1",role="primary"} 1

        metriks ini

     3.hasura_postgres_pool_wait_time_bucket{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",le="0.3",role="primary"} 1

       metriks ini

* hasura_postgres_pool_wait_time_sum{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1.6099813e-2

  metriks ini menunjukkan
  
* hasura_postgres_pool_wait_time_count{conn_info="HASURA_GRAPHQL_DATABASE_URL",source_name="default",role="primary"} 1

  metriks ini menunjukkan 


```
# HELP hasura_scheduled_trigger_request_bytes_total Total size of HTTP request bodies sent via scheduled triggers (experimental)
# TYPE hasura_scheduled_trigger_request_bytes_total counter
hasura_scheduled_trigger_request_bytes_total 0.0
```
* hasura_scheduled_trigger_request_bytes_total 0.0

  metriks ini menunjukkan


```
# HELP hasura_scheduled_trigger_response_bytes_total Total size of HTTP response bodies received via scheduled triggers (experimental)
# TYPE hasura_scheduled_trigger_response_bytes_total counter
hasura_scheduled_trigger_response_bytes_total 0.0
```
* hasura_scheduled_trigger_response_bytes_total 0.0

  metriks ini menunjukkan 

```
# HELP hasura_websocket_connections Current number of active WebSocket connections
# TYPE hasura_websocket_connections gauge
hasura_websocket_connections 0.0
```

* hasura_websocket_connections 0.0

  metriks ini menunjukkan 


```
# HELP hasura_websocket_message_queue_time The time (in seconds) for which a websocket message remains queued in the GraphQL engine's websocket queue
# TYPE hasura_websocket_message_queue_time histogram
hasura_websocket_message_queue_time_bucket{le="1.0e-6"} 0
hasura_websocket_message_queue_time_bucket{le="1.0e-4"} 0
hasura_websocket_message_queue_time_bucket{le="1.0e-2"} 0
hasura_websocket_message_queue_time_bucket{le="0.1"} 0
hasura_websocket_message_queue_time_bucket{le="0.3"} 0
hasura_websocket_message_queue_time_bucket{le="1.0"} 0
hasura_websocket_message_queue_time_bucket{le="3.0"} 0
hasura_websocket_message_queue_time_bucket{le="10.0"} 0
hasura_websocket_message_queue_time_bucket{le="30.0"} 0
hasura_websocket_message_queue_time_bucket{le="100.0"} 0
hasura_websocket_message_queue_time_bucket{le="+Inf"} 0
hasura_websocket_message_queue_time_sum 0.0
hasura_websocket_message_queue_time_count 0
```



```
# HELP hasura_websocket_message_write_time The time taken (in seconds) to write a websocket message into the TCP send buffer
# TYPE hasura_websocket_message_write_time histogram
hasura_websocket_message_write_time_bucket{le="1.0e-6"} 0
hasura_websocket_message_write_time_bucket{le="1.0e-4"} 0
hasura_websocket_message_write_time_bucket{le="1.0e-2"} 0
hasura_websocket_message_write_time_bucket{le="0.1"} 0
hasura_websocket_message_write_time_bucket{le="0.3"} 0
hasura_websocket_message_write_time_bucket{le="1.0"} 0
hasura_websocket_message_write_time_bucket{le="3.0"} 0
hasura_websocket_message_write_time_bucket{le="10.0"} 0
hasura_websocket_message_write_time_bucket{le="30.0"} 0
hasura_websocket_message_write_time_bucket{le="100.0"} 0
hasura_websocket_message_write_time_bucket{le="+Inf"} 0
hasura_websocket_message_write_time_sum 0.0
hasura_websocket_message_write_time_count 0
```



```
# HELP hasura_websocket_messages_received_bytes_total Total size of WebSocket messages received
# TYPE hasura_websocket_messages_received_bytes_total counter
hasura_websocket_messages_received_bytes_total 0.0
```








  .

