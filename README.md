:spiral_calendar: Atualizado em 20 de Março de 2021 :heart:

<img align="right" alt="GIF" height="160px" src="https://github.com/rdeconti/rdeconti-resources/blob/main/Digital%20Innovation%20One%20-%20Logotipo.png" />

# Projeto Digital Innovation One: Bootcamp Impulso FullStack Developer 

# Sistema de classificados

Crie um sistema de classificados com Ruby on Rails
Este projeto foi proposto pela Digital Innovation One - Link do código original: não existente no GitHub
Professor: Carlos Ribeiro
Aulas: https://web.digitalinnovation.one/lab/criando-um-sistema-de-classificados-com-ruby-on-rails/learning/cda71d14-9cc6-48cf-820b-c6933f947b56

# Descrição

Neste Labs iremos desenvolver em duas etapas um sistema completo de classificados, produzindo do zero ao deploy em produção junto testes automatizados, tendo como base a tecnologia Ruby on Rails.

# Detalhes técnicos

- Ruby version: ruby 2.7.2p137 (2020-10-01 revision 5445e04352) [x64-mingw32]
- Rails vercdsion: Rails 6.1.3
- yarn version: v1.22.10
- devise version: 4.7.3
- Rspec
   -- rspec-core (3.10.0)
   -- rspec-expectations (3.10.0)
   -- rspec-mocks (3.10.0)
   -- rspec-rails (4.0.1)
   -- rspec-support (3.10.0)

# Passos para executar (comandos executados no Visual Studio Code)

- Ajustar as versões dos GEMs no arquivo GemFile (diretório raiz do projeto)
- bundle install
- Foram encontrados problemas para instalar NOKOGIRI
-- ridk exec pacman -S mingw-w64-x86_64-libxslt
-- gem install nokogiri --platform=ruby -- --use-system-libraries
-- substitui o GemFile.lock pelo GemFile.Lock do MindApp
- yarn install --check-files
- bundle install
- rails db:create
- rails db:migrate
- rails server



# Melhorias implementadas

- Implementação do Bootstrap para melhorar a apresentação das telas 
- utilizei as recomendações desta páginas:
- https://cliente.widhost.com.br/knowledgebase/127/Como-adicionar-o-Bootstrap-a-um-aplicativo-Ruby-on-Rails.html)
- https://betterprogramming.pub/how-to-add-stimulus-js-to-a-rails-6-application-4201837785f9
- Instalar o Boostrap com: yarn add bootstrap jquery popper.js
- Atualizar este arquivo: / rails-bootstrap / config / webpack / environment.js

      const { environment } = require('@rails/webpacker')
      const webpack = require("webpack") 

      environment.plugins.append("Provide", new webpack.ProvidePlugin({ 
      $: 'jquery',
      jQuery: 'jquery',
      Popper: ['popper.js', 'default']
      }))  

      module.exports = environment

- Atualizar este arquivo:  / rails-bootstrap / app / javascript / packs / application.js

      yarn add stimulus 

      import { Application } from "stimulus"
      import { definitionsFromContext } from "stimulus/webpack-helpers"

      import "bootstrap"
      import "../stylesheets/application"

- Crie um diretório para as folhas de estilo: mkdir app/javascript/stylesheets
- Crie o arquvio: / rails-bootstrap / app / javascript / stylesheets / application.scss 
      @import "~bootstrap/scss/bootstrap";
      @import url('https://fonts.googleapis.com/css?family=Merriweather:400,700');

# Exemplos de telas

<img src="https://github.com/rdeconti/Projeto-DIO-Ruby-Sistema-De-Classificados/blob/main/tela.jpg" />
