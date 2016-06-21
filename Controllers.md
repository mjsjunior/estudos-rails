### View & Controller

Cada método criado no controller é uma action, que pode ser acessada através de um browser.

Para escrever na saída, o Rails oferece o comando render, que recebe uma opção chamada "text" (String). Tudo aquilo que for passado por esta chave será recebido no browser do cliente.

[Fonte](https://www.caelum.com.br/apostila-ruby-on-rails/controllers-e-views/#9-2-hello-world) e [Video](https://www.youtube.com/watch?v=GY7Ps8fqGdc)

#### Criando um controller

```
generate controller name_controller name_action_controller

```

Ao se criar um controller ele se encontra em 

``` 
apps/controllers/nome_controller.rb 
```
Também é criado uma VIEW, que sera administrada por este controller.

```
/app/view/nome_controller
```
E dentro desta pasta cada ACTION do controller é responsavel por um arquivo .html.erb

#### Criando Rota
Logo após criar o controller é preciso configurar a rota em que este controller ira trabalhar. Para isso acesse o arquivo config/routes.rb e adicione as configurações de rotas necessarias.

```
match 'inicio' => 'home#index', via: 'get'
```
Quando uma requisição GET for realizada em /inicio o controller Home será chamado na sua função INDEX. A mesma situação pode ser escrita desta form

```
match 'categorias/:nome', controller: 'categorias', action: 'show', via: 'get'
```

[SOBRE ROTAS](/Routes.md)