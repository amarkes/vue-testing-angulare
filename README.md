# Front-end Vue.js Developer @ Angular e-Commerce e Pagamentos Digitais
se você chegou até aqui, é porque tem os pre requisitos sitados [aqui](https://github.com/vuejs-br/vagas/issues/213)

### Sobre o teste
1. para qualquer dúvida deverá ser aberta uma issue, afinal sua dúvida pode ser a do próximo
1. ao publicar o projeto no github, certifique que o mesmo esteja privado (para nenhum candidato colar do outro) e dê permissão para os usuários ( amarkes )
1. ative o github pages no projeto (pode ver mais sobre neste [link](https://www.treinaweb.com.br/blog/criando-paginas-para-repositorios-com-o-github-pages/), iremos olhar a parte funcional pelo github pages


### o candidato deverá:
1. usar o Vue cli
1. publicar seu teste no github (Privado) para que seja feita a revisão no código e visual
1. usar as boas praticas do Vue js
1. criar uma aplicação web component, o candidato pode saber mais sobre web component neste [artigo](https://medium.com/@thulioph_/web-components-com-vue-js-9a21f6dea3cc)
1. criar uma aplicação que possa ser inserida em qualquer pagina web

### Projeto

- [ ] criar um novo projeto com nome de wip-angulare
- [ ] implementar o bootstrap para os estilos do projeto
- [ ] criar uma pagina (amostra) para mostrar os components que serão desenvolvidos
- [ ] criar uma estrutura baseada no modelo abaixo conforme nescessidade
```
│ common
│ ├─ classes
│ ├─ directives
│ ├─ functions
│ └─ mixins
├─ components
├─ plugins
│ └─ validators
└─ stores
```

### componente de cadastro

- [ ] criar um botão na pagina de amostra para abrir um modal (com botão de fechar no footer do modal) ( iremos chamar de modal de cadastro)

+ devemos criar um formulário contendo os seguintes campos
  + Nome completo
  + Email (Validação de email)
  + Data de nascimento (mascara para DD/MM/YYYY)
  + Telefone (mascara para (99) 99999-9999)
  + Sexo (drodown com Masculino e Feminino)
  + T-Shirt Masculina/Feminina (mostrar de acordo com o que foi selecionado no sexo)

salvar em store (ao da refresh na pagina esses dados não existirão)

- [ ] criar um botão na pagina de amostrar, este botão irá abrir um outro modal (com botão de fechar no footer do modal), neste modal iremos mostrar em uma tabela, os dados salvos no store do modal de cadastro, a tabela irá exibir os campos Nome, email, data de nascimento, telefone, sexo, t-shirt e ações
+ Botoes de ações serão ( Alterar e Deletar )
  + ao clicar em alterar deverá abrir o modal de cadastro passando os dados deste item e ao salvar as alterações irá substituir o item no store
  + ao clicar em deletar ele irá mostrar um alerta pedindo confirmação, se for confirmado o item deverá ser deletado do store

### componente de post
- [ ] fazer a instalação do axios
- [ ] criar serviços (pode conferir a documentação [aqui](https://jsonplaceholder.typicode.com/guide/)
+ criar um método para pegar um único post (get)
  + endpoint https://jsonplaceholder.typicode.com/posts/ID
+ criar um método para pegar uma lista (getAll)
  + endpoint https://jsonplaceholder.typicode.com/posts
+ criar um método para fazer um post (post)
  + endpoint https://jsonplaceholder.typicode.com/posts
  + campos title, body, userId
+ criar um método para fazer um put (put)
  + endpoint https://jsonplaceholder.typicode.com/posts/ID
  + campos id, title, body, userId
+ criar um método para fazer um patch (patch)
  + endpoint https://jsonplaceholder.typicode.com/posts/ID
  + campos title, body, userId
+ criar um método para fazer um delete (delete)
  + endpoint https://jsonplaceholder.typicode.com/posts/ID

- [ ] criar um botão que irá abrir uma modal (com botão de cancelar no footer do modal) e nesta modal, termos uma tabela que irá listar os post pegando o método de list (getAll), mostrando os campos title, body, userId, ação, acima desta tabela teremos um botão de adicionar post
+ teremos ações de alterar e deletar em cada linha da tabela
  + ao clica em alterar envia o item do post para um outro modal com o formulario e botoes de alterar e cancelar
    + alterar irá fazer um put
    + cancelar irá fechar o modal
+ teremos ação de deletar, irá abrir um alerta perguntando se deseja deletar o item, caso seja confirmado devemos chamar o método de delete
- [ ] Botão de adicionar do modal acima, irá abrir um outro modal contendo o formulário (campos title, body e userId tudo texto) com botoes de salvar e cancelar
+ ações dos botoes
  + ao clicar em salvar irá chamar o método post e salvar os dados
  + ao clicar em cancelar fecha o modal
