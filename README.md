## Projeto

Serviço utilizando API Rest em Java (Quarkus) que prove informações de dados da fatura de uma cartão disponível em base de dados.


## Build
mvn clean package


## Execução local
mvn quarkus:dev -Ddebug=false


# ============================
# Execução via docker-compose
# ============================

docker-compose --env-file ./.env up


# =====================================
# Geração de Chaves públicas e privadas
# =====================================

# gerando chave privada
openssl genrsa -out rsaPrivateKey.pem 2048

# gerando chave pública
openssl rsa -pubout -in rsaPrivateKey.pem -out publicKey.pem

# convertendo chave privada formato PKCS#8
openssl pkcs8 -topk8 -nocrypt -inform pem -in rsaPrivateKey.pem -outform pem -out privateKey.pem

# Autor
Reinaldo Jesus Santana - reinaldojsantana@gmail.com



![image](https://user-images.githubusercontent.com/17239827/225924264-26923df8-1484-442c-95b8-60e7db8ad3cf.png)
