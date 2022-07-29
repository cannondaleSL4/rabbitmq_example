#docker run -d --name some-rabbit -e RABBITMQ_DEFAULT_USER=dmba -e RABBITMQ_DEFAULT_PASS=dmba -v /home/USER/rabbitmq/:/home/dima/data/rabbitmq -p 4369:4369 -p 5671:5671 -p 5672:5672 -p 15672:15672 rabbitmq

#docker run -d --name some-rabbit -p 5672:5672 -p 5673:5673 -p 15672:15672 rabbitmq:3-management


# Run rabbitMq docker image

docker run -d --name rabbitmq \
--hostname rabbitmq \
-v /home/USER/rabbitmq/:/home/dima/data/rabbitmq \
-p 5672:5672 -p 5673:5673 -p 15672:15672 \
rabbitmq:3-management

# Proto generate
protoc --java_out=./src/main/java/ ./src/main/java/com/dmba/**/*.proto