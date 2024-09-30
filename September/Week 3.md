# Minggu Ke 3 September 2024
# Setting VPN, Akses Rancher dan Deploy Hasura

## Setting VPN 
Koneksikan VPN yang sudah di dapatkan dengan Pritunl.
[Dokumentasi penggunaan Pritunl](https://docs.google.com/document/d/12waQ-Z15AeJ61NZ48Avke8BO27v_Oc5e/edit?usp=drive_link&ouid=106095707560747597119&rtpof=true&sd=true)

## Koneksi atau Menyambungkan ke Rancher
Setelah VPN terhubung, gunakan informasi di bawah ini untuk login ke Rancher :
- **URL:** `https://10.100.13.175/`
- **User:** `devteams`
- **Password:** `K4wah1j3n2024`
- **Cluster Kubernetes:** `cluster-k8s-alldataint`

## Deploy Hasura 
Setelah login, silahkan untuk melakukan deploy hasura, menyesuaikan dengan namespace yang sudah dibuat.

Untuk list server dan juga namespace dapat dilihat pada file berikut [List Server.xlsx](https://github.com/user-attachments/files/17197355/List.Server.xlsx)


Berikut adalah kode yang saya gunakan :

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  labels:
    app: hasura
    hasuraService: custom
  name: hasura-uthar
  namespace: uthar
spec:
  replicas: 1
  selector:
    matchLabels:
      app: hasura-uthar
  template:
    metadata:
      labels:
        app: hasura-uthar
    spec:
      containers:
      - image: hasura/graphql-engine:v2.42.0
        imagePullPolicy: IfNotPresent
        name: hasura
        env:
        - name: HASURA_GRAPHQL_DATABASE_URL
          value: postgres://uthar:uthar@10.100.13.205:/uthar
        - name: HASURA_GRAPHQL_ENABLE_CONSOLE
          value: "true"
        - name: HASURA_GRAPHQL_DEV_MODE
          value: "true"
        ports:
        - name: http
          containerPort: 8080
          protocol: TCP
        livenessProbe:
          httpGet:
            path: /healthz
            port: http
        readinessProbe:
          httpGet:
            path: /healthz
            port: http
        resources: {}
```



## Menambahkan Service untuk Hasura pada Rancher
Setelah melakukan Deployment untuk Hasura selanjutnya, kita harus menambahkan service untuk hasura tersebut.

Berikut contoh file untuk Service pada hasura yang saya gunakan :

```yaml
apiVersion: v1
kind: Service
metadata:
  labels:
    app: hasura-uthar
  name: hasura-uthar
  namespace: uthar
spec:
  ports:
  - protocol: TCP
    port: 8087
    targetPort: 8080
  selector:
    app: hasura
  type: LoadBalancer
```


