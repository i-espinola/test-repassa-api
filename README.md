# Test Repassa API

## Instalação

**NOTA:** Para executar qualquer um dos comandos abaixo, é imprescindível ter o gerenciador de dependencia NPM instalado globalmente em seu computador, e nagevar para dentro do diretório root da aplicação para que todos os comandos possam ser executados com sucesso.

### Instalação local

Para fazer a instalação de todas as dependencias da aplicação, execute a seguinte linha de comando no terminal.

    npm install

**Nota**: Se após a intalação você receber informações de vulnerabilidades nas dependencias instaladas, execute o seguinte comando para corrigir eventuais vulnerabilidades.

    npm audit fix && npm audit fix --force

### Modo desenvolvimento

Os arquivos do código fonte da aplicação estão contidos dentro do diretório `./src`.
Após concluir a instalação de todas as dependencias da aplicação, é possível executar o comando de desenvolvimento no terminal.

    npm run dev

Depois de executar o comando acima, a aplicação estará pronta para receber as requisições a partir dos endpoints da API.
A aplicação sera recompilada sempre que você salvar um arquivo, você também verá quaisquer eventuais erros no código no seu console.

### Modo debugger

Os arquivos do código fonte da aplicação estão contidos dentro do diretório `./src`.
Após concluir a instalação de todas as dependencias da aplicação, é possível executar o comando de desenvolvimento para degubar a aplicação.

    npm run debugger

Depois de executar o comando acima, a aplicação estará pronta para receber as requisições a partir dos endpoints da API.
A aplicação sera recompilada sempre que você salvar um arquivo, você também verá quaisquer eventuais erros no código no seu console.

### Modo produção

Com esse comando será inicializado um servidor **_Express_** e executara os arquivos de **produção** no diretório `./build`, que por padrão, busca o arquivo `index.js`.

    npm run start

### Construção (Transpilar)

Este comando cria os arquivos de produção dentro do diretório `./build`. Os arquivos de produção são transpilados e minificados para obter uma melhor performance e otimização de trafego de dados ao acessar a aplicação. Para construir a aplicação em modo producão, execute o seguinte comando.

    npm run build

**Nota**: Se você possui um servidor local capaz de executar aplicações web, e quiser publicar o projeto com o comando `npm run build`, não se esqueça de ajustar o caminho relativo no arquivo `./package.json` na propriedade `homepage:`.

## Uso da API

Esta API faz operações CRUD a partir de requisições recebidas via protocolo HTTP. A URL da API em questão é:

    https://repassa-api.herokuapp.com/api

### Criar novo funcionário - POST

Para criar um novo funcionário basta enviar uma requisição com o método `POST` com os parametros *name*, *login*, *feedback* com o prefixo `/create` logo após a URL da API.
Desta forma a requisição deve ser assim:

    https://repassa-api.herokuapp.com/api/create?name=kiko&login=kikinho&feedback=Criança mimada, e não muito inteligente.

Esta requisição returna o objeto criado do usuário.

### Atualizar funcionário - PUT

Para atualizar um funcionário basta enviar uma requisição com o método `PUT` com os parametros *name*, *login*, *feedback*, e informar o ID do funcionário logo após a URL da API.
Desta forma a requisição deve ser assim:

    https://repassa-api.herokuapp.com/api/5def8be15ee04b004c0ab78d?name=kiko&login=tesouro&feedback=Criança mimada, e não muito inteligente.

Esta requisição returna o objeto atualizado do usuário em questão.

### Deletar funcionário - GET

Para deletar um funcionário basta enviar uma requisição com o método `DELETE` com o respectivo ID do funcionário logo após a URL da API.
Desta forma a requisição deve ser assim:

    https://repassa-api.herokuapp.com/api/5def8be15ee04b004c0ab78d

Esta requisição returna o objeto deletado do usuário.

### Buscar funcionário - GET

Para buscar um funcionário basta enviar uma requisição com o método `GET` com o respectivo ID do funcionário logo após a URL da API.
Desta forma a requisição deve ser assim:

    https://repassa-api.herokuapp.com/api/5def8be15ee04b004c0ab78d

Esta requisição returna o objeto do usuário solicitado.

### Listar todos funcionários - GET

Para listar todos funcionário basta enviar uma requisição com o método `GET` com o sufixo `/list` logo após a URL da API.
Desta forma a requisição deve ser assim:

    https://repassa-api.herokuapp.com/api/list

Esta requisição returna um objeto com todos os usuários persistidos na base.

## Principais tecnologias integradas

- [x] Babel.
- [x] ESlint.
- [x] Express.
- [x] Git.
- [x] JavaScript - **ES6**.
- [x] MongoDB.
- [x] Nodejs.
- [x] Nodemon.
- [x] NPM.
