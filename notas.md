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


### 

```ruby

```



### 

```ruby

```



### 

```ruby

```



### 

```ruby

```



### 

```ruby

```

