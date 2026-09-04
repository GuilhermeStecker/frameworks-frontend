# 📚 Aula — Consumindo APIs no Front-end

Nesta aula foi abordado como aplicações **Front-end se comunicam com outros sistemas por meio de APIs**. Os principais assuntos foram **API, REST, protocolo HTTP, métodos HTTP, endpoints, JSON, servidor Backend, Web Services e Express.js**, além da publicação de uma API utilizando o **Render**. 

---

## 🔌 O que é uma API?

**API (Application Programming Interface)** significa **Interface de Programação de Aplicações**.

Uma API é um conjunto de protocolos, rotinas e ferramentas que define **como diferentes sistemas ou componentes de software podem se comunicar**. 

De forma simplificada:

```text
Front-end
   ↓
  API
   ↓
Back-end / Servidor
   ↓
Banco de Dados
```

Por exemplo, uma aplicação Front-end pode solicitar informações para uma API e depois utilizar os dados recebidos para atualizar a página.

---

# 🌐 API REST

Também foi apresentado o conceito de **REST (Representational State Transfer)**, um estilo arquitetural utilizado principalmente no desenvolvimento de sistemas distribuídos para Web.

Uma API seguindo os princípios REST utiliza:

* 🔄 Comunicação entre **cliente e servidor**;
* 🧠 Comunicação **stateless**;
* 🌐 Métodos HTTP;
* 🔗 Recursos identificados por **URIs**;
* 📦 Representações de dados, como **JSON**. 

### 🧠 O que significa Stateless?

Significa que **cada requisição é independente**.

Ou seja, o servidor não precisa "lembrar" automaticamente das requisições anteriores para processar a próxima. Esse conceito também aparece entre as principais características do protocolo HTTP apresentadas na aula. 

---

# 🌍 Protocolo HTTP

O **HTTP (Hypertext Transfer Protocol)** é o protocolo responsável pela comunicação na Web.

Ele estabelece as regras utilizadas para a troca de informações entre:

```text
Cliente                         Servidor
(Navegador / Front-end)   ↔    (Back-end)
```

O cliente realiza uma **requisição** e o servidor envia uma **resposta**. 

---

# 📡 Métodos HTTP

As requisições HTTP possuem diferentes métodos de acordo com aquilo que queremos realizar.

| Método         | Função                              |
| -------------- | ----------------------------------- |
| **GET** 🔎     | Buscar/recuperar informações        |
| **POST** ➕     | Criar um novo recurso               |
| **PUT** 🔄     | Substituir completamente um recurso |
| **PATCH** ✏️   | Atualizar parcialmente um recurso   |
| **DELETE** 🗑️ | Remover um recurso                  |

### 🔎 GET

Utilizado para **recuperar informações do servidor**. Não deve alterar os dados.

### ➕ POST

Utilizado para **criar novos recursos** no servidor.

### 🔄 PUT

Utilizado para **substituir completamente** um recurso existente.

### ✏️ PATCH

Utilizado para **atualizar apenas parte** de um recurso.

### 🗑️ DELETE

Utilizado para **remover um recurso específico**. 

Uma maneira simples de lembrar:

```text
GET     → Buscar
POST    → Criar
PUT     → Substituir
PATCH   → Atualizar
DELETE  → Excluir
```

---

# 🔄 Como funciona uma requisição?

A aula mostrou o processo completo de comunicação entre Front-end e servidor.

### 1️⃣ Usuário realiza uma ação

O usuário acessa uma página ou clica em algum botão.

### 2️⃣ Front-end envia uma requisição

O navegador envia uma requisição HTTP:

```text
GET / POST / PUT / DELETE
```

### 3️⃣ Backend recebe

O servidor, no exemplo da aula utilizando **Express.js**, identifica a rota e executa a lógica necessária. 

### 4️⃣ Dados são processados

O servidor pode buscar, gravar ou atualizar informações em um banco de dados ou utilizar uma API externa.

### 5️⃣ Servidor responde

Após processar a solicitação, o servidor pode retornar os dados em formato **JSON**.

### 6️⃣ Front-end atualiza a página

Finalmente, o Front-end recebe a resposta e apresenta os dados ou uma mensagem ao usuário. 

Resumindo:

```text
👤 Usuário
   ↓
🖥️ Front-end
   ↓ Requisição HTTP
⚙️ Backend / API
   ↓
🗄️ Banco de Dados
   ↓
⚙️ Backend
   ↓ Resposta JSON
🖥️ Front-end
   ↓
👤 Usuário vê o resultado
```

---

# 🔗 Endpoint

Um **endpoint** é uma **URL específica que permite acessar determinado recurso ou funcionalidade de uma API**.

Ele funciona como um ponto de comunicação entre cliente e servidor. 

Por exemplo, uma API poderia possuir:

```text
/usuarios
/produtos
/clientes
/pedidos
```

O método HTTP utilizado junto ao endpoint determina a ação que será realizada.

Por exemplo:

```text
GET /usuarios
```

Busca usuários.

Enquanto:

```text
POST /usuarios
```

poderia adicionar um novo usuário.

---

# 🌎 APIs Públicas

Também foi apresentada a possibilidade de utilizar **APIs públicas** para desenvolver aplicações.

Existem catálogos que reúnem APIs disponibilizadas por diferentes projetos e serviços, permitindo encontrar dados para integrar em aplicações Front-end. 

Isso permite criar aplicações utilizando informações fornecidas por outros sistemas sem precisar criar todos os dados do zero.

---

# 📦 JSON

O **JSON (JavaScript Object Notation)** é um formato leve utilizado para troca de dados.

Suas principais características são:

* 👨‍💻 Fácil para humanos lerem e escreverem;
* 🤖 Fácil para máquinas interpretarem e gerarem;
* 🔑 Pode representar pares de **nome/valor**;
* 📋 Pode representar listas ordenadas por meio de **arrays**. 

### Exemplo de objeto JSON

```json
{
  "nome": "Carlos Silva",
  "idade": 20,
  "ativo": true
}
```

### Exemplo com array

```json
{
  "frutas": ["maçã", "banana", "laranja"]
}
```

A **página 12** mostra justamente exemplos visuais dessas duas estruturas: objetos com propriedades e arrays contendo vários valores.

---

# 🖥️ Servidor Backend

Na segunda parte da aula, o foco passou para a criação de uma API.

Um **servidor Backend** é responsável por:

* 📥 Receber e processar requisições;
* 🗄️ Armazenar e recuperar dados;
* ⚙️ Executar regras de negócio;
* 📤 Fornecer respostas;
* 🔌 Disponibilizar APIs para outros sistemas. 

Portanto, enquanto o Front-end representa aquilo com que o usuário interage, o Backend fica responsável pelo **processamento e gerenciamento das informações**.

---

# 🌐 Web Service

Um **Web Service** é um serviço acessível pela Web que permite que diferentes sistemas se comuniquem utilizando **HTTP/HTTPS**.

Uma característica importante é permitir comunicação entre sistemas desenvolvidos com **diferentes linguagens, plataformas ou tecnologias**, utilizando uma comunicação padronizada. 

---

# 🟢 Express.js

O **Express.js** foi apresentado como um framework para **Node.js** que facilita a criação de servidores Web e APIs.

Ele é:

* 🪶 Minimalista;
* ⚡ Leve e rápido;
* 🔧 Flexível;
* 🌐 Muito utilizado no ecossistema JavaScript. 

---

## ⚙️ Por que utilizar Express?

Utilizar apenas Node.js pode exigir uma quantidade maior de código para lidar com rotas e outras funcionalidades.

O Express simplifica tarefas como:

* 🛣️ **Roteamento** → criação de rotas como `/users` e `/products`;
* 🔧 **Middlewares** → processamento de requisições e respostas;
* 🔐 Autenticação;
* 📋 Logs;
* ⚡ Criação rápida de APIs e servidores Web. 

Na **página 21**, a aula compara visualmente um servidor criado com **Node.js puro** e outro utilizando **Express.js**, mostrando como o Express permite realizar a mesma ideia com uma estrutura mais simples. 

---

# 🛠️ Criando uma API REST com Express

A aula também apresentou os passos básicos para criar uma API.

### 1️⃣ Criar o projeto

Primeiro, deve-se criar uma pasta para o projeto e abri-la no VS Code.

### 2️⃣ Instalar o Express

```bash
npm install express
```

### 3️⃣ Instalar o CORS

```bash
npm install cors express
```



### 4️⃣ Criar `api.js`

O arquivo:

```text
api.js
```

é utilizado para configurar o servidor e suas rotas.

### 5️⃣ Executar

```bash
node api.js
```



---

# 🔐 CORS

O **CORS** foi apresentado como um mecanismo de segurança que controla o acesso entre **domínios diferentes no navegador**. 

Ele é importante quando, por exemplo, temos:

```text
FRONT-END
site.com
   ↓
requisição
   ↓
BACK-END
api.com
```

Como são origens diferentes, o CORS participa do controle dessa comunicação.

---

# 🚀 Quando utilizar Express.js?

Segundo a aula, o Express pode ser utilizado principalmente para:

* Criar **APIs REST**;
* Integrar aplicações com bancos de dados;
* Desenvolver Backends para aplicações Web e Mobile;
* Trabalhar com templates;
* Utilizar middlewares para autenticação, logs e tratamento de erros;
* Criar protótipos rapidamente. 

---

# ☁️ Render

A aula também apresentou o **Render** como uma plataforma de hospedagem em nuvem que pode ser utilizada para disponibilizar a API na Internet.

Entre as características apresentadas estão:

* ☁️ Hospedagem na nuvem;
* 🟢 Suporte a Node.js;
* 🐍 Suporte a Python e outras linguagens;
* 🌿 Integração com repositórios Git;
* 🔄 Deploy contínuo;
* 🔒 Certificado SSL;
* 📈 Possibilidade de escalabilidade;
* 🔌 Uso para APIs e microsserviços. 

---

# 📤 Deploy da API

O processo apresentado para colocar a API online foi:

```text
Projeto local
     ↓
GitHub
     ↓
Render
     ↓
Web Service
     ↓
API disponível online 🌐
```

Primeiro, o projeto deve estar disponível em um repositório no **GitHub**.

Depois, cria-se um novo **Web Service** no Render e conecta-se o repositório. 

O comando de inicialização apresentado foi:

```bash
node api.js
```

Após o deploy, a API passa a possuir um endereço online que poderá ser utilizado pelo Front-end. 

---

# 📝 Atividade 01

A primeira atividade consiste em pesquisar **10 projetos no GitHub que utilizem APIs**.

Para cada projeto, deve-se:

1. 🔎 Pesquisar o projeto;
2. 📥 Clonar e analisar;
3. 🧩 Identificar o framework utilizado;
4. 🔌 Identificar as APIs consumidas;
5. 📄 Criar um arquivo Markdown;
6. 📊 Montar uma tabela detalhando os projetos e suas informações. 

---

# 🛠️ Atividade 02

Na segunda atividade, deve ser criada uma **API utilizando Express**, contendo uma rota que retorne **data e hora**.

Depois:

```text
API Express
    ↓
GitHub
    ↓
Render
    ↓
API online
    ↓
Front-end
    ↓
Exibe data e hora
```

O Front-end deve consumir essa API e apresentar a **data e hora na tela**. 

Além disso, a API e o Front-end devem ficar em **repositórios separados**.

A documentação da atividade deve conter:

* 📸 Prints do código;
* 🖥️ Prints da aplicação funcionando;
* ☁️ Prints dos painéis do Render e Vercel;
* 🔗 Links dos repositórios no GitHub;
* 📄 Organização das informações em um documento para entrega. 

---

# 📝 Resumo Geral

A aula **“Consumindo APIs no Front-end”** mostrou como ocorre a comunicação entre uma aplicação Front-end e um servidor.

Os conceitos principais podem ser resumidos assim:

```text
🔌 API
   ↓
🌐 HTTP
   ↓
📡 GET / POST / PUT / PATCH / DELETE
   ↓
🔗 Endpoint
   ↓
📦 JSON
   ↓
🖥️ Backend
   ↓
🟢 Node.js + Express
   ↓
☁️ Deploy no Render
   ↓
💻 Front-end consome a API
```

O ponto central da aula foi compreender que o **Front-end pode solicitar ou enviar informações para um Backend através de uma API**, utilizando requisições HTTP. O servidor processa essas requisições e pode retornar dados em **JSON**, que são utilizados pela interface.

Além da parte conceitual, a aula introduziu a **criação de uma API REST com Express.js**, sua publicação online utilizando o **Render** e, por fim, a integração dessa API com uma aplicação Front-end.
