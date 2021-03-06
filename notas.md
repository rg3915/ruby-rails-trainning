# Ruby

## Como instalar o Ruby

https://www.ruby-lang.org/pt/documentation/installation/

```bash
ruby -v
```

```bash
gem -v
gem list
```

```bash
gem install rails
```

## Generators

```bash
rails new appexample
```

Como rodar o servidor

```bash
cd appexample
rails server
```

## Bundler

Gerenciador de gems instaladas.

```bash
bundle install
```

## Interpretador Ruby

```bash
irb
```

ou

```bash
gem install pry
gem install pry-require_relative
pry
```

### Exemplos

```ruby
a = 1
b = 2
if a < b
  puts 'a é menor que b'
end
```

```ruby
while a < 10
  puts a
  a += 1
end
```

## Ruby - Array, Hash, Métodos, Parâmetros e Blocos

### Array

```ruby
a = []
a.push(2)
a.push(10)
a.push("ruby")
b = %w(curso de ruby on rails)
b[2]
```

### Hash (Dicionário)

```ruby
myhash = {"chave" => "valor", "linguagem" => "Ruby"}
myhash["chave"]
```

### Métodos

```ruby
a.size
```

### Parâmetros

```ruby
a.size.eql?(2)
```

### Blocos

```ruby
b = %w(curso de ruby on rails)
b.each do |items|
  puts items
end
```

### Classes

```ruby
a = 123
a.class
nome = 'Texto'
a.class
```

```ruby
class Pessoa
  def falar
    puts "Oi"
  end
end

pessoa = Pessoa.new
pessoa.falar
pessoa.class
```

```ruby
cd appexample/tmp
irb
require_relative "pessoa"
pessoa = Pessoa.new
pessoa.falar
```

```ruby
irb
require_relative "atleta"
atleta = Atleta.new
atleta.class
atleta.correr
atleta.falar
```

### Módulos

Um módulo é uma coleção de métodos e constantes.

```ruby
cd appexample/tmp
irb
require_relative "meu_modulo"
Configuracoes::NOME_DO_SISTEMA
include Configuracoes # módulo dentro da classe
```


### Mixins

```ruby
cd appexample/tmp
irb
require_relative "meu_mixin"
mm = MeuMixin.new
mm.calcular
mm.enviar_correio
```


### Yield

```ruby
def ola
  puts "Ola"
  yield
  puts "Oi"
end

ola {puts "Eu aqui no meio"}
```


### Banco de Dados

`config/database.yml`

### Rake

Ferramenta de gerenciamento de tarefas.

```
cd appexample
rake -T
rake db:create
```

### Rails

**Convention over configuration** e **Scaffold**

```
cd appexample
rails generate scaffold customer name:string email:string birthday:date obs:text
```

### Migrations

```
rake db:migrate
```

### Views, Embedded Ruby

Em `views/customers/index.html.erb`

```ruby
<% a = "Rails" %>

texto A --- <%= a -%>
```

### Textos interpolados com variáveis

```ruby
<%= "teste #{a} on #{b} teste" %>
```

### Rails Console

```
rails console # ou rails c
a = Customer.first
a.name
b = Customer.all
```

### Variáveis de Instância

`controllers/customers_controller.rb`

```ruby
@customers = ...
```

### Rotas

`config/routers.rb`

```bash
rails g controller welcome
```

```ruby
Rails.application.routes.draw do
  root 'welcome#index'

  resources :customers

  get 'inicio' => 'welcome#index'
end
```

### Controllers

`controllers/welcome-controller.rb`

```ruby
class WelcomeController < ApplicationController
  def index
    @teste = "Curso de Rails"
  end
end
```

### Helpers

`views/welcome/index.html.erb`

```html
<h1>Teste de página INDEX na WELCOME CONTROLLER!</h1>
<h3><%= @teste %></h3>
<%= link_to "Cadastro de Clientes", customers_path %>
```

### Symbols x Strings

`:texto` e `"texto"`.
```

### Active Record

```ruby
rails console
x = Customer.all
x = Customer.last
y = Customer.where(:id => 1) #ou
y = Customer.where(id: 1)
z = Customer.create(name: "Maria", email: "maria@example.com", birthday: Date.today, obs: "Lorem ipsum...")
w = Customer.new
w.name = "Joaquim"
w.email = "joaquim@example.com"
w.birthday = Date.today
w.obs = "Lorem ipsum..."
w.save
```

### Controllers

### Filtros

before_action x before_filter


### Partials

`_sua_partial.html.erb`

```ruby
<%= render 'form' %>
```

### Helpers

`form_for`, `f.label`, `f.text_field`, `f.submit`

### Params

```ruby
@parametros = params
```

### i18n

`config/application.rb`

```ruby
module Appexample
  class Application < Rails::Application
    config.i18n.default_locale = "pt-BR"
  end
end

```

```bash
touch config/locales/pt-br.yml
```

```ruby
"pt-BR":
  hello: "Olá Mundo"
```

```
i18n.t # traduz
i18n.l # localiza data
```

https://github.com/svenfuchs/rails-i18n

https://github.com/svenfuchs/rails-i18n/blob/master/rails/locale/pt-BR.yml

Renomeei para `pt-br_rails.yml`

### Bootstrap Rails

https://github.com/seyhunak/twitter-bootstrap-rails

```ruby
# Gemfile
gem "twitter-bootstrap-rails"
```

```bash
bundle install
rails generate bootstrap:install static
rails g bootstrap:layout application fluid
rails g bootstrap:themed Customers
```

## Criando uma aplicação

**App:** Agenda

```bash
rails new remember
rails g scaffold Annotation body:text
rails g scaffold Friend name:string address:string email:string phone:string
rails db:migrate
```

http://localhost:3000/rails/info/routers

```bash
rails g controller welcome index
```

```bash
bundle install
rails generate bootstrap:install less
rails generate bootstrap:install static
rails g bootstrap:layout application fluid
rails g bootstrap:themed Annotations
rails g bootstrap:themed Friends
```


### i18n

Estando na pasta `remember` digite

```bash
wget -O config/locales/pt-br_rails.yml https://raw.githubusercontent.com/svenfuchs/rails-i18n/master/rails/locale/pt-BR.yml

```

### Pagination

https://github.com/mislav/will_paginate

https://github.com/amatsuda/kaminari

```ruby

```

### 

```ruby

```

