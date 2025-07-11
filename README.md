### Visão Geral

Uma plataforma de e-commerce com funcionalidades de catálogo, autenticação e gerenciamento básico de produtos.

### Funcionalidades Implementadas:

**Frontend Moderno e Responsivo:** Design com HTML5 e CSS3, utilizando Flexbox e Grid para layout adaptável a qualquer dispositivo (desktops, tablets, celulares), inspirado em grandes lojas de tecnologia.

**Autenticação de Usuários:** Sistema completo de registro e login com segurança (criptografia de senha com bcryptjs e autenticação por JWT - JSON Web Tokens).

**Gerenciamento de Sessão:** Reconhecimento do status de login do usuário, exibindo o nome de usuário no cabeçalho e um menu dropdown personalizado com opções de conta e logout.

**Painel Administrativo:** (Acesso restrito a administradores) Permite a listagem de todos os usuários cadastrados e a gestão de suas permissões (tornar admin/remover admin).

**Criação de Anúncios de Venda:** (Acesso restrito a administradores) Formulário dedicado para adição de novos itens ao catálogo, com informações como nome, descrição, preço, estoque, categoria e URL de imagem.

**Navegação por Categorias:** Páginas dedicadas para cada seção principal (Categorias, Lançamentos, Promoções, Jogos Digitais, Moedas In-Game, Skins & Itens, Pré-Vendas, Suporte).

**Chatbot de Suporte:** Assistente virtual interativo na página de suporte com respostas pré-definidas para as perguntas frequentes dos usuários.

**Elementos Visuais Dinâmicos:** Incorporação de um banner de oferta flutuante e seções de destaque de produtos com navegação por abas.

**Rodapé Informativo:** Estrutura de rodapé completa com links úteis e ícones de redes sociais.

Tecnologias Utilizadas

### Tecnologias

* **Frontend:** HTML5, CSS3, JavaScript (ES6+) 

* **Backend:** Node.js, Express.js 

* **Banco de Dados:** MongoDB (NoSQL) 

* **ORM/ODM:** Mongoose 

* **Autenticação/Autorização:** JWT (JSON Web Tokens), bcryptjs 

* **Ferramentas:** npm, Git 


Como Rodar o Projeto
Instruções claras e concisas para que qualquer um possa clonar seu repositório e rodar o projeto localmente.

### Como Rodar o Projeto

Siga os passos abaixo para configurar e executar o projeto em sua máquina local.

**Pré-requisitos:**

Node.js (versão LTS recomendada)

npm (gerenciador de pacotes do Node.js)

MongoDB Community Server (rodando na porta padrão 27017)

Git


1. **Clone o Repositório:**

Bash

git clone https://github.com/DaviSCR05/OpenINgame
cd OpenINgame

2. **Configure o Backend:**

Navegue até a pasta do backend:


cd OpenINgame-Backend-Node
Instale as dependências:


npm install
Crie um arquivo .envna raiz da pastaOpenINgame-Backend-Node e adicione as seguintes variáveis:

Snippet de código

MONGO_URI=mongodb://localhost:27017/opengame_db
PORT=5000
JWT_SECRET=crieumasenha_!




**Crie um Usuário Administrador no MongoDB:**

Para acessar o painel de administração e criar anúncios, você precisará de um usuário com isAdmin: true no banco de dados.

Recomenda-se usar o [MongoDB Compass](https://www.mongodb.com/products/compass) para conectar-se ao seu banco (mongodb://localhost:27017/opengame_db) e inserir um novo documento na coleção users.

**Importante:** A senha deve ser criptografada. Você pode usar um script temporário Node.js com bcryptjs para gerar o hash da sua senha.


{
  "username": "superadmin",
  "email": "admin@example.com",
  "password": "COLE_O_HASH_AQUI",
  "isAdmin": true
}
Inicie o servidor backend:

node server.js

(O servidor estará rodando em http://localhost:5000.)

3. **Acesse o Frontend:**

Mova os arquivos do frontend (index.html, login.html, css/, js/, img/, etc.) para dentro da pasta public no diretório do seu backend (OpenINgame-Backend-Node/public/).

Com o servidor backend rodando, abra seu navegador e acesse:

http://localhost:5000/# OpenINgame
