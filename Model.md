### Models

Models são os modelos que serão usados nos sistemas: são as entidades que serão armazenadas em um banco.

### Criando um novo modelo
```
rails generate model restaurante
```

### Migrations
Migrations ajudam a gerenciar a evolução de um esquema utilizado por diversos bancos de dados. Foi a solução encontrada para o problema de como adicionar uma coluna no banco de dados local e propagar essa mudança para os demais desenvolvedores de um projeto e para o servidor de produção.

Com as migrations, podemos descrever essas transformações em classes que podem ser controladas por sistemas de controle de versão (por exemplo, git) e executá-las em diversos bancos de dados.

Sempre que executarmos a tarefa Generator -> model, o Rails se encarrega de criar uma migration inicial, localizado em db/migrate.

[Fonte](https://www.caelum.com.br/apostila-ruby-on-rails/active-record/#7-7-migrations)