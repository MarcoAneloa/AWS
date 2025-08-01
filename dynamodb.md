Comandos
* Levantar una base dynamodb en local con docker

* Operaciones en la tabla
 - aws dynamodb create-table --cli-input-json file://create_table.json --endpoint-url=http://localhost:8000
 - aws dynamodb create-table --table-name Music  --attribute-definitions AttributeName=Artist,AttributeType=S AttributeName=SongTitle,AttributeType=S --key-schema AttributeName=Artist,KeyType=HASH AttributeName=SongTitle,KeyType=RANGE --billing-mode=PAY_PER_REQUEST --endpoint-url http://localhost:8000
 - aws dynamodb describe-table --table-name Music --endpoint-url http://localhost:8000
 - aws dynamodb update-table --table-name Music --provisioned-throughput ReadCapacityUnits=20,WriteCapacityUnits=10 --endpoint-url http://localhost:8000
 - aws dynamodb delete-table --table-name Music --endpoint-url http://localhost:8000
 - aws dynamodb list-tables --endpoint-url=http://localhost:8000

* Opraciones en el Item
- aws dynamodb scan --table-name nameTable --endpoint-url=http://localhost:8000
- aws dynamodb batch-write-item --request-items file://items_table.json --endpoint-url=http://localhost:8000
  
