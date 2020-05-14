
Connect to Kafka:

kubectl -n clients run kafka-producer -ti --rm=true --restart=Never \
 --image=strimzi/kafka:0.14.0-kafka-2.3.0 -- bin/kafka-console-producer.sh \
   --broker-list my-cluster-kafka-bootstrap.kafka:9093 --topic my-topic

Look at Broker logs: 

kubectl logs my-cluster-kaf ka-0 -n kafka -c kafka -f


# Shell interactif
kubectl exec -n clients -ti kafka-client-shell /bin/bash


