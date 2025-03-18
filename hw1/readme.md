1. Скачал и разархивировал архив kafka_2.12-3.9.0.tgz с сайта https://kafka.apache.org/downloads
2. запустил zookeaper c ссылкой на файл конфигурации из дистрибутива.
   .\zookeeper-server-start.bat ..\..\config\zookeeper.properties
   Cкриншот (zookeaperStarted.jpg)
3. запустил сервер кафки с ссылкой на файл конфигурации из дистрибутива.
   .\kafka-server-start.bat D:\apache\kafka_2.12-3.9.0\config\server.properties 
   скриншот (kafkaStarted.jpg)
4. Создал топик test (.\kafka-topics.bat --bootstrap-server localhost:9092 --create --topic test --partitions 1 --replication-factor 1)
5. Записал в него сообщения (.\kafka-console-producer.bat --topic test --bootstrap-server localhost:9092)
6. Начал читать сообщения (.\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning)
Скриншоты по 4-6 пункту - topicCreatedMessageWriteRead.jpg
