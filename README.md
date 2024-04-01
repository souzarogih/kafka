<h2>
    Repositório com configurações de container kafka e spring/boot para rodar no docker.
</h2>

### Containers

#### zookeeper
    image: confluentinc/cp-zookeeper:latest

Serviço de coordenação distribuída utilizado pelo kafka.
    
#### kafka
    image: confluentinc/cp-kafka:latest

Serviço de mensageria para fila Kafka

#### kafdrop
    image: obsidiandynamics/kafdrop:latest
    
Interface para consulta e análise dos payloads do Kafka.
  
#### payment
    image: higorsouza/payment-service:1.0.1

Microservice Java/Spring para receber dados de um requisição http e enviar para processamento na fila do Kafka.

#### consumer
    image: higorsouza/jsonconsumer:1.0.1

Microservice Java/Spring usado para consumir os payloads na fila do Kafka.

#### Acessar Kafka Drop
`http://localhost:19000`