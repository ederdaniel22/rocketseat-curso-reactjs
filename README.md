Iniciamos o projeto com: 
## yarn init -y

Instalamos o React com: 
## yarn add react

instalamos o react-dom com: 
## yarn add react-dom.

Criamos a pasta src com os arquivos index.jsx e App.jsx

instalamos o babel com: 
## yarn add @babel/core @babel/cli @babel/preset-env
usando o babel criamos o dist/bundle.js com o comando 
## yarn babel src/index.jsx --out-file dist/bundle.js
na raiz do projeto criamos e configuramos o babel.config.js 

Instalamos o webpack com: 
## yarn add webpack webpack-cli  
E na raiz criamos o arquivo webpack.config.js

criamos a pasta public e nela o arquivo index.html

## para rodar o projeto usamos yarn webpack

para o browser enxergar o javascrit do html:
instalamos webpack-plugin com: 
## yarn add html-webpack-pluggin -D

fizemos a importação da extensão no wepack.config.js com:
## const HtmlWebpackPlugin = require('html-webpack-plugin)
Atualizamos o webpack.config.js

Instalamos o weback server com: 
## yarn add webpack-dev-server -D
atualizamos as configurações no webpack config com a linha abaixo do resolve
## devServer: {
##    contentBase: path.resolve(__dirname, 'public')
##    },
essa configuração vai automatizar a reinicialização

Para rodar o projeto a partir dessa configuração usamos
## yarn webpack serve

Configurar o source-map no webpack.config.js para visualizar erros na aplicação
no module.exports abaixo do mode devlopment inserir:
## devtool: 'eval-source-map',

Criar a variável NODE_ENV com:
## NODE_ENV=production yarn webpack

Instalar o CrossEnv
## yarn add cross-env -D

criar no package json os scripts
## "scripts":{
##    "dev": "webpack serve",
##    "build": "cross-env NODE_ENV=production webpack"
##  },

A partir desse momento para rodar o projeto usamos 
## yarn dev

Criar pasta styles e dentro dela o arquivivo:
## global.css

criar no webpack.config.js mais um rules para que o projeto entenda css também
Retirar deste rules o babel loader, instalar as dependências 
## yarn add style-loader css-loader -D
depois inserir a linha:
## use: ['style-loader', 'css-loader', 'sass-loader']

Atualizamos a aplicação instalando o sass
## yarn add node-sass -D
## yarn add sass-loader D