# API para chat serverless integrado com API do OpenAI ChatGPT para a AWS Cloud Week

## Passos para o projeto

- Clonar o repositório
- Instalar as dependências com o comando ```npm install```
- Atualizar o arquivo ```.env``` com a sua chave do OpenAI
- Compactar o conteúdo do projeto em um arquivo ```.zip```

## Na AWS

- Acessar o console da AWS
- Criar uma função no serviço AWS Lambda
- Fazer o upload do conteúdo do arquivo ```.zip``` no código da função
- Acessar o serviço AWS API Gateway
- Criar uma API Websocket
- Criar os endpoints (obs: os três primeiros endpoints marcados com ```$``` são padrão de uma API Websocket do API Gateway):
    - ```$connect```
    - ```$disconnect```
    - ```$default```
    - ```setName```
    - ```sendPublic```
    - ```sendPrivate```
    - ```sendBot```

## Testando o Websocket

- Baixar a dependência ```wscat``` através do comando ```npm i -g wscat```. 
- Utilizar o parâmetro ```-g``` para instalar de forma global no sistema operacional, podendo chamá-la de fora do projeto.

### Utilizando o wscat

- ```wscat -c url_de_conexao_do_websocket```
- Exemplo de chamada ```{"action":"sendPublic", "message":"Hello World!"}```

### Utilizado Amazon API Gateway

É um serviço de gerenciamento de APIs totalmente gerenciado que torna mais fácil para os desenvolvedores criar, publicar,
manter, monitorar e proteger APIs RESTful e WebSocket em qualquer escala.

### Utilizado AWS Lambda

O AWS Lambda é um serviço de computação sem servidor e orientado a eventos que permite executar código para praticamente qualquer tipo de aplicação ou serviço de backend sem provisionar ou gerenciar servidores. Você pode acionar o Lambda a partir de mais de 200 serviços da AWS e aplicações de software como serviço (SaaS) e pagar apenas pelo que usar.
