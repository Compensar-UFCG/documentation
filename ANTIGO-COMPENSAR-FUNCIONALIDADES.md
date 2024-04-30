# Funcionalidades do Antigo Compensar

Descrição do Ambiente
Desenvolvedores: Erick Costa e Marcelo Vitorino
Orientadores: Cláudio Campelo e Lívia Sampaio
Versão 01










Essa documentação tem como objetivo descrever as telas existentes na primeira versão do ambiente apresentando as possibilidades que o usuário possui ao utilizar a ferramenta. O documento apresenta o ambiente a partir de uma descrição textual acrescida de screenshots. Essa versão do ambiente pode ser encontrada em: https://compensarufcg.herokuapp.com/

Agenda
Início
Navbar
Sobre
Contato
Cadastro
Meus Dados 
Edição
Buscar Questões
Primeira Página
Página Principal
Exibição
Edição
Remoção
Criar Questões
Objetiva e Subjetiva
Sugestões





Início
Objetivo: Apresentar de forma concisa a descrição do ambiente, com destaque ao que o profissional da educação pode realizar com o uso da ferramenta. 

“Proporcionar ao profissional de educação que o Pensamento Computacional possa ser desenvolvido de maneira interdisciplinar à disciplina de Matemática.”
Navbar
Contém links, na mesma ordem, para as seguintes páginas: Início (Atual); Buscar Questões; Criar Questões; Sobre; Contato. Além de um dropdown com links para Meus Dados e Minhas Questões.
Sobre
Descreve de forma introdutória ao usuário a principal funcionalidade do ambiente: Criação de Questões; Além da possibilidade de criar listas de exercícios (ainda não explorada na primeira versão do ambiente)
 
Criando Questões;
Criando Lista de Exercícios.
Contato
Contém um formulário que permite ao usuário escrever uma mensagem e enviá-la ao email aepc.lacina@gmail.com. 


<img width="600" alt="Captura de Tela 2024-04-30 às 17 12 17" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/bb22758e-c1db-414a-8392-3ff8abbdbd45">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 12 27" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/e2c125c4-d922-4786-a8d5-58ce84aa3a76">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 12 39" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/425b1e3e-f345-49a3-bec9-47921759d3c0">


Conjunto de Figuras 1 - Tela Inicial


Cadastro
Objetivo: Registrar o usuário no ambiente e coletar informações sobre o seu perfil. 

O perfil do usuário coletado contém informações sobre: Idade; Cargo; Cidade; Instituição. 

O sistema não permite que o usuário acesse as páginas de Buscar e Criar Questões caso o mesmo não tenha o cadastro registrado no ambiente.  


<img width="600" alt="Captura de Tela 2024-04-30 às 17 13 28" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/59dfab69-a6e6-4693-b1bd-0ca69be1a6cf">

Figura 2 - Tela de Cadastro


Meus Dados
Objetivo: Apresentar as informações recuperadas do usuário com sessão ativa no ambiente e permitir a edição de seus dados.
Edição
Proporciona ao usuário atualizar seus dados quando necessário. 


<img width="600" alt="Captura de Tela 2024-04-30 às 17 13 36" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/92a89e1e-6638-456e-b6c5-c54c799ab46a">



Figuras 3 - Meus Dados


Buscar Questões
Primeira Página (Por conteúdo e competências)
Objetivo: Permitir que o usuário realize a busca inicial de forma rápida e simples. Possibilitando a seleção de questões pelo conteúdo da matemática e pelas competências do Pensamento Computacional.

Ao utilizar o campo de conteúdo, denota-se a possibilidade de obter como retorno um conjunto de questões daquela área da matemática. Além da utilização da seleção de competências, que utilizada em conjunto ao campo de conteúdo, pode retornar um conjunto de questões de um conteúdo específico da Matemática que possua alguma das competências selecionadas.

O ambiente permite que o usuário busque por questões sem selecionar um conteúdo e/ou competências específicas.
Página Principal (Por todos os campos e operações em questões)
Objetivo: Permitir que o usuário realize a busca por questões, incluindo busca avançada (com todas os campos de uma questão). Visualização de páginas de questões retornadas da busca. Como também visualizar as questões filtradas pelo usuário com sessão ativa (Minhas Questões). 

Durante as buscas por termos do enunciado, aqueles documentos que possuem esse termo exibem-o de forma destacada.
Buscas
Realiza o mesmo sistema de buscas da primeira página com acréscimo da opção de busca avançada. Que permite também a realização de buscas pelos campos de Enunciado, Tipo, Fonte e Autor.

Descrição de execução de buscas:

Conteúdo: Retorna questões que possuam match exato com o conteúdo.
Competências: Retorna questões com uma ou mais competências selecionadas. 
Ordem de retorno:
Questões com menos competências, das quais essas fazem match com a maior quantidade dentre as competências buscadas;
Questões com mais competências, das quais essas fazem match com a maior quantidade dentre as competências buscadas;

Enunciado: Retorna questões com presença ou ausência o termo buscado.
Ordem de retorno:
Questões com maior frequência do termo buscado e que possuam menor enunciado;
Questões com maior frequência do termo buscado e que possuam maior enunciado;
Fonte/Autor: Retorna questões que façam match com no mínimo uma palavra dentre o conjunto de palavras buscadas. Case insensitive. Para o campo Fonte: caso mesmo que existam documentos contendo a mesma palavra buscada com uma frequência maior que um, as questões serão retornadas com a mais atual cadastrada no ambiente como prioritária.
Competências E Enunciado: Considera os valores dos dois campos unidos (competências e enunciado) de forma textual. Documentos que fazem uma maior quantidade de matchs para Competências ou Enunciado e que possuam um menor valor na união dos dois campos terão prioridade maior. 
Competências E/OU Enunciado + outro(s) campo(s): Outro(s) campo(s) serão analisados inicialmente (de forma individual como descrito acima), seguido pela análise de competências e/ou enunciado (de forma individual ou em dupla como descrito acima).
Minhas Questões
Retorna questões filtradas pelo campo autor preenchidas automaticamente com o nome do usuário com sessão ativa. Permite realizar buscas avançadas mantendo o filtro por autor.
Exibição
Exibe por padrão questões contendo o conteúdo, enunciado e competências. É exibido por padrão apenas um trecho do enunciado. Além de um botão para ver os detalhes da questão. 

Detalhes da questão:
Exibição de um modal com todos os campos da questão, além de botões que permitem edição e remoção da questão. O campo enunciado é exibido de forma completa.
Edição
Proporciona ao usuário atualizar os valores de uma questão quando necessário. Questões com o campo de enunciado atualizado também atualizam automaticamente o campo de competências.
Remoção
Permite remover uma questão cadastrada.




<img width="600" alt="Captura de Tela 2024-04-30 às 17 14 21" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/e1192919-cce7-44ee-897e-a6883bf14646">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 14 28" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/5623cff2-b64a-422f-8b3f-d31dd87b8540">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 14 50" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/3611108a-f1b5-4df3-9162-11665fd0bb55">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 14 44" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/086bad5a-23fe-4d2f-aefe-79f7fdfd5633">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 14 39" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/d5369c90-c261-498c-a5f1-b5072a52eab3">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 14 33" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/0e00c192-f7b2-4564-998a-80dc5c83ead1">

Conjunto de Figuras 4 - Tela de Buscar Questões


Criar Questões
Objetivo: Registrar uma nova questão Objetiva ou Subjetiva no sistema. E durante o processo de criação, receber um feedback com as competências que foram identificadas após a inserção do enunciado da questão.

Todos os campos são obrigatórios. O usuário só avança durante o processo de criação após o preenchimento dos campos exibidos.

Toda questão possui: Conteúdo, Fonte, Enunciado, Tipo e Competências. Questões Subjetivas possuem também o campo Espelho enquanto Questões Objetivas possuem o campo Alternativas.
Objetiva e Subjetiva
Permite que o usuário crie questões com os campos gerais e que a partir da escolha do tipo (Objetiva ou Subjetiva) possibilita o acréscimo de um espelho de resposta da questão ou da adição de alternativas para a questão.

O campo de alternativas permite a sinalização da alternativa correta.




<img width="600" alt="Captura de Tela 2024-04-30 às 17 17 15" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/98e5c2e5-1af5-496e-9ce4-a551b38a8bc3">
<img width="600" alt="Captura de Tela 2024-04-30 às 17 17 21" src="https://github.com/Compensar-UFCG/documentation/assets/20846737/80207e85-fc67-4ba7-ac8c-85dc8a5268e1">





Conjunto de Figuras 5 - Tela de Criar Questões


Sugestões
Login: Criar login interno do sistema.
Cadastro: Durante o cadastro, exibir um modal pedindo a permissão ao usuário da utilização dos dados para análises de dados internas.
Início: Colocar a seta inicial apontada para baixo de forma dinâmica, assim como está a seta que aponta para cima ao realizar scroll down da tela.
Geral: Deixar as telas responsivas. (Apenas as telas de Meus dados, Cadastro, Criar Questões e exibição das questões possuem algum avanço na responsividade).
Buscas: Para os inputs de fonte, autor e enunciado exibir sugestões e armazenar novas.
Buscas: Melhorar a barra com as páginas de questões, não só apresentando a primeira e última página como opção para clique.
Geral: Realizar melhorias com nível de prioridade baixo que estão descritas nessa planilha.



