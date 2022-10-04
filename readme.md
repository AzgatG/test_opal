### The Graph

## Запускаем локально graph-node
1. Клонируем https://github.com/graphprotocol/graph-node
2. cd graph-node/docker
3. В докер файле меняем
 environment.ethereum: 'mainnet:https://rpc-opal.unique.network'
4. docker-compose up
## Генерим локально subgraph из ABI файла
1. Устанавливаем CLI npm install -g @graphprotocol/graph-cli
2. graph init --from-contract contractAddress --abi ./abi.json prefix/graphName directory. Генерится subgraph для контракта из abi - пример https://github.com/AzgatG/test_opal
3. Меняем в файле subgraph.yaml dataSources.source.startBlock - стартовый блок для сканирования контракта
4. npm run create-local
5. npm run deploy-local - деплоим subgraph в локальный graph-node


## Пример контракта с ABI
Адрес - 0xED83A4E878E496ec1C84BdBbbC50c6657181F906
ABI - ./abi.json
