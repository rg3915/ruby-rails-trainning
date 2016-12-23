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

```

### Módulos

```ruby

```


### Mixins

```ruby

```


### Yield

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



### 

```ruby

```

