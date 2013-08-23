---
layout: post
title: "Como alterar o nome de um projeto Rails"
date: 2013-08-23 14:46
comments: true
categories: 
---

Para começar uma dica bastante simples, mas que me foi bastante útil: Como alterar o nome de um projeto Rails. Obs: O procedimento abaixo é válido apenas para Rails 3

**Instale o plugin “Rename” em seu projeto:**

``` console
rails plugin install git@github.com:get/Rename.git
```

**Para alterar o nome digite o seguinte comando:**

```ruby
rails g rename_to ["NOVO_NOME"]
```

Os seguintes arquivos serão alterados:

``` console
config/application.rb
config/environment.rb
config/environments/development.rb
config/environments/test.rb
config/environments/production.rb
config/routes.rb
config.ru
config/initializers/secret_token.rb
config/initializers/session_store.rb
``` 

**Uma vez que o nome tenha sido alterado o plugin pode ser removido:**

``` ruby
rm -r "vendor/plugins/Rename"
``` 

Espero que venha a ser útil, um grande abraço a todos!