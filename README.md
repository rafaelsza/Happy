<p align="center">
    <img src="assets/header-happy-logo.png" alt="Proffy"/>
</p>

<p align="center">
Projeto construído durante a Next Level Week #3 da Rocketseat.
</p>

<div align="center">

  ![](https://img.shields.io/badge/language-typescript-blue)
  ![](https://img.shields.io/badge/server-nodejs-brightgreen)
  ![](https://img.shields.io/badge/web-reactjs-blue)
  ![](https://img.shields.io/badge/mobile-react%20native-blueviolet)
  ![](https://img.shields.io/badge/database-mariadb-yellowgreen)
  ![](https://img.shields.io/badge/license-MIT-sucess)

</div>

Proffy é um projeto que foi desenvolvido para que pessoas encontrem Casas de Acolhimento Institucional para irem fazer uma visita e levar alegria para as crianças e adolecentes que moram lá.

### ✅ Funcionalidades:

- Pessoas responsáveis por essas Casas de Acolhimento Institucional podem realizar um cadastro informando endereço, uma descrição, instruções de visita, horário aberto e se aceita visitas no final de semana.
- Pessoas interessadas em realizar uma visita podem verificar no mapa onde tem uma casa para que possam fazer uma visita.

### 🛠 Tecnologias:

- [**React**](https://pt-br.reactjs.org/), [**TypeScript**](https://www.typescriptlang.org/), [**NodeJS**](https://nodejs.org/en/), [**Yarn**](https://yarnpkg.com/), [**Expo**](https://expo.io/) e [**MariaDB**](https://mariadb.org/).

- 🖥 Server (API)
    - [**express**](https://expressjs.com/pt-br/) -> Para criar as rotas do back-end.
    - [**typeorm**](https://typeorm.io/) -> ORM (Object Relational Mapper).
    - [**mysql**]() -> Driver para conexão do typeorm com o banco de dados MariaDB.
    - [**multer**](https://github.com/expressjs/multer) -> Para realizar o upload de arquivos.
    - [**yup**](https://github.com/jquense/yup) -> Validação de dados.
- 🌐 Web
    - [**axios**](https://github.com/axios/axios) -> Realizar a conexão com nosso back-end.
    - [**react-router-dom**](https://reactrouter.com/web/guides/quick-start) -> Criar a navegação da nossa aplicação.
    - [**leaflet**](https://leafletjs.com/) -> Biblioteca para uso de mapas.
    - [**react-leaflet**](https://react-leaflet.js.org/) -> Integrar a biblioteca leaflet com nossa aplicação React.
- 📱 Mobile
    - [**axios**](https://github.com/axios/axios) -> Realizar a conexão com nosso back-end.
    - [**react-native-maps**](https://github.com/react-native-maps/react-native-maps) -> Para utilização de mapas em nosso app.
    - [**react-native-gesture-handler**](https://github.com/software-mansion/react-native-gesture-handler) -> Navegação nativa de dispositivos móveis.
    - [**react-navigation**](https://reactnavigation.org/) -> Navegação de telas da aplicação.

### 📝 Padronização de código utilizando:

EditorConfig, ESLint e Prettier.

## ➡ Para utilizar em sua máquina:

**Necessário ter o 
[NodeJS](https://nodejs.org/en/download) 
instalado.**

> No projeto foi utilizado o 
[yarn](https://yarnpkg.com/getting-started/install)
como gerenciador de pacotes, mas caso queira utilizar o npm basta substituír os comandos que começam com yarn por npm.

Para utilizar as rotas do projeto será preciso utilizar o 
[Insomnia](https://insomnia.rest/download)
ou o 
[Postman](https://www.postman.com/downloads)
, conforme sua preferência.

### 🖥 Back-end

> Altere o arquivo **_ormconfig.example.json_** na pasta _server_ com os dados da sua conexão com o banco de dados, após isso alterar o nome para **_ormconfig.json_**

```
# Clone o projeto:

$ git clone https://github.com/rafaelsza/Happy.git


# Entre na pasta raíz do projeto:

$ cd Happy


# Entre na pasta server e execute yarn para instalar as dependências

$ cd server && yarn


# Agora rode as migrations para criar as tabelas no banco de dados:

$ yarn typeorm migration:run


# Para executar o projeto digite:

$ yarn api
```

Agora com o Back-end rodando em sua máquina já pode começar a utilizar as rotas e seus métodos HTTP.

### 🔀 Métodos HTTP e suas rotas:

**ROTA**: [http://localhost:3333/orphanages]()

- **POST**: para cadastrar uma nova Casa de Acolhimento Institucional no banco de dados.

  Crie uma nova requisição do tipo POST no Insomnia/Postman colocando a rota acima e passando dentro do corpo os valores em formato Multipart, conforme exemplificados abaixo:
  ```json
  {
    "name": "Mundo Feliz",
    "latitude": "-25.3736458",
    "longitude": "-49.4085648",
    "about": "Sobre o orfanato",
    "instructions": "Instruções do orfanato",
    "opening_hours": "Das 8hrs às 18hrs",
    "open_on_weekends": "true",
    "images": [
      {
        "path": "1602719123684-download.jpg",
        "id": 13
      }
    ]
  }
  ```
  > Em _images_ deve ser usado um campo do tipo File e adicionado as imagens que queria enviar.

- **GET**: retorna todas as Casas de Acolhimento Institucional cadastradas no banco de dados.

  Crie uma nova requisição do tipo GET no Insomnia/Postman colocando a rota acima.

**ROTA**: [http://localhost:3333/orphanages/:id]()

- **GET**: Retorna os dados de uma Casa de Acolhimento Institucional.

  Crie uma nova requisição do tipo GET no Insomnia/Postman colocando a rota acima informando o ID que deseja receber os dados.

### 🌐 Front-end Web
> Lembrando que seu back-end deve estar rodando para poder utilizar os front-ends web e mobile.

```
# Volte na pasta raíz do projeto e entre em web

$ cd .. && cd web


# Execute yarn para instalar as dependências

$ yarn


# Para executar o projeto digite:

$ yarn start
```

### 📱 Front-end Mobile
> Lembrando que seu back-end deve estar rodando para poder utilizar os front-ends web e mobile.

> Para utilizar o front-end mobile baixe no seu celular um aplicativo chamado Expo.

```
# Volte na pasta raíz do projeto e entre em web

$ cd .. && cd mobile


# Execute yarn para instalar as dependências

$ yarn


# Para executar o projeto digite:

$ yarn start
```

No navegador que abrir, abra o aplicativo do Expo no seu celular e aponte ele para escanear o QRCode e executar o app no seu celular.

## 📃 Licença

Esse repositório está licenciado pela MIT LICENSE, confira o arquivo LICENSE deste repositório.

 <h3 align="center">👨🏻‍💻 Feito por <a href="https://www.linkedin.com/in/rafael-souza-28aa621ab/">Rafael Souza</a></h3>
