# Documentação Arquitetural do Compensar

A arquitetura do nosso sistema é estruturada conforme o C4 Model, que fornece uma abordagem visual para descrever a arquitetura de software em diferentes níveis de abstração. Nossa aplicação é projetada para proporcionar uma experiência interativa e eficiente para os usuários, seja através de navegadores web ou dispositivos móveis.

Essa arquitetura foi projetada para proporcionar uma experiência de usuário fluida e uma estrutura de software escalável e robusta, capaz de atender às demandas de um ambiente dinâmico e em constante evolução.

# Contexto

![image](https://github.com/Compensar-UFCG/documentation/assets/20846737/ba3e1029-4886-4650-9e5c-4c0e6a48ae6f)

A interação do usuário com o frontend ocorre por meio de requisições HTTPS, permitindo uma comunicação segura entre o cliente e o servidor. Nosso frontend oferece diversas funcionalidades essenciais, incluindo cadastro, login, visualização de questões, criação de listas de questões e a possibilidade de baixar essas listas para acesso offline. Essas funcionalidades são acessíveis tanto via web quanto em aplicativos móveis, garantindo flexibilidade e conveniência para os usuários.

Por trás do frontend, temos o backend, que é responsável por fornecer os serviços necessários para atender às solicitações dos clientes. Nosso backend é construído como uma API RESTful, seguindo os princípios de CRUD (Create, Read, Update, Delete) para as entidades de usuário, questão e competência do pensamento computacional. Essa API é acessada pelo frontend por meio de requisições HTTP, permitindo uma comunicação eficiente e padronizada entre as camadas do sistema.

Para armazenar e gerenciar os dados da aplicação, utilizamos o banco de dados MongoDB, um banco de dados NoSQL altamente escalável e flexível. O backend se comunica com o MongoDB para realizar operações de persistência e recuperação de dados, garantindo integridade e consistência das informações em toda a aplicação.






