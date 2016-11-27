Instalação:
1 - Faça o download da versão 3.2.10 do MongoDB
2 - Crie uma variável de ambiente e logo em seguida verifique a versão do mongo no prompt com o comando: mongo -version

Roteiro de configuração:
1 - Descompacte o arquivo "MONGO_CONFIG" onde quiser. Sugestão C:\Java\data_base.
2 - Abra no modo edit o arquivo "mongo_server.bat" e configure uma pasta para criação do bando. OBS.: Função que precisa ser executada somente na 1º vez, depois rode o .bat para executar o servidor. 
2 - Rode o script de criação do bando com o seguinte comando: mongo --shell <caminho do arquivo>\collections.js
3 - Logo após o mongo iniciara o modo client, verifique se as coleções foram criadas com o seguinte comando: db.getCollectionNames()
4 - Logo em seguida saia do client digitando exit.
5 - Importe a coleção de usuários com o seguinte comando: mongoimport -c user --jsonArray < <caminho dos arquivos>\user.json
6 - Importe a coleção de serviços com o seguinte comando: mongoimport -c service --jsonArray < <caminho dos arquivos>\service.json
7 - Entre no client com o comando: mongo
8 - Verifique os dados da coleção user como comando: db.user.find().pretty()
9 - Verifique os dados da coleção service como comando: db.service.find().pretty()
