# 📚 Aula 02 — Configuração do Ambiente de Desenvolvimento

Nesta aula foram apresentados os principais conceitos e ferramentas necessários para preparar um **ambiente de desenvolvimento Front-end**, abordando versionamento de código, Git, VS Code, Node.js, NPM, criação de projetos React e deploy com Vercel. 

---

## 🔄 Versionamento de Software

O **versionamento** é utilizado para registrar e controlar as diferentes versões de um projeto. Cada alteração pode ser identificada, permitindo saber **o que foi modificado, quem realizou a mudança e quando ela aconteceu**. 

Diferente de um simples **backup**, o versionamento mantém um histórico completo das alterações e facilita o trabalho de várias pessoas no mesmo projeto.

### Principais benefícios:

* 👥 Trabalho simultâneo entre desenvolvedores;
* 🔍 Histórico e rastreabilidade das alterações;
* ↩️ Recuperação de versões anteriores;
* 🛡️ Menor risco de perda de código;
* 🔀 Uso de branches para trabalhar em mudanças sem afetar a versão principal. 

---

## 🔢 Versionamento Semântico — SemVer

O **Versionamento Semântico (SemVer)** utiliza o padrão:

```text
MAJOR.MINOR.PATCH
```

Exemplo:

```text
2.1.3
```

Cada número possui um significado:

* **MAJOR** → mudanças incompatíveis com versões anteriores;
* **MINOR** → novas funcionalidades compatíveis com a versão anterior;
* **PATCH** → correções de bugs. 

Exemplo de evolução:

```text
1.0.0 → Primeira versão estável
1.1.0 → Nova funcionalidade
1.1.1 → Correção de bug
2.0.0 → Mudança incompatível com versões anteriores
```

O SemVer facilita o gerenciamento de dependências e torna mais clara a evolução do software. 

---

## 💻 IDE e Visual Studio Code

Uma **IDE (Integrated Development Environment)** reúne ferramentas utilizadas para **desenvolver, testar, executar e depurar software**.

O **Visual Studio Code (VS Code)** é um editor de código que pode oferecer diversos recursos típicos de uma IDE através de extensões e ferramentas integradas. 

---

## 🌿 Git e Controle de Versão

O **Git** é um sistema de controle de versão utilizado para acompanhar as alterações realizadas nos arquivos de um projeto.

Com ele é possível:

* Registrar diferentes versões do projeto;
* Acompanhar mudanças;
* Restaurar versões anteriores;
* Enviar código para repositórios online;
* Baixar e sincronizar código. 

Após a instalação, ela pode ser verificada com:

```bash
git --version
```

Também é possível configurar o usuário:

```bash
git config --global user.name "Nome"
git config --global user.email "email"
```

---

## 🏷️ Tags e boas práticas no Git

As **tags** são marcadores utilizados para identificar pontos importantes do histórico do projeto, como versões estáveis:

```bash
git tag 1.0.0
```

Para enviar uma tag ao repositório:

```bash
git push origin 1.0.0
```

Elas ajudam a organizar os lançamentos e versões importantes do projeto. 

### ✅ Boas práticas

Durante o desenvolvimento, é recomendado:

* Fazer **commits pequenos e frequentes**;
* Escrever mensagens de commit claras;
* Manter a branch principal estável;
* Criar branches para funcionalidades e correções;
* Testar o código antes de realizar um **merge**. 

---

## 🟢 Node.js

O **Node.js** é um ambiente que permite executar **JavaScript fora do navegador**, inclusive no backend/servidor.

Isso permite utilizar JavaScript tanto no **Front-end quanto no Back-end**, facilitando a integração entre as duas partes da aplicação. 

Para verificar a instalação:

```bash
node --version
```

---

## 📦 NPM — Node Package Manager

O **NPM** é o gerenciador de pacotes do Node.js e é instalado junto com ele.

Ele permite:

* Instalar bibliotecas e frameworks;
* Atualizar e remover pacotes;
* Gerenciar dependências;
* Compartilhar módulos;
* Automatizar a configuração das dependências de um projeto.

O arquivo **`package.json`** registra as dependências utilizadas. Assim, ao baixar um projeto, é possível instalar os pacotes necessários utilizando:

```bash
npm install
```



---

## ⚛️ Criação de Projetos React

A aula também apresentou a criação de uma aplicação **React** utilizando o `create-react-app`.

```bash
npx create-react-app meu-projeto-react
```

Depois, é possível acessar o projeto e executá-lo:

```bash
cd meu-projeto-react
code .
npm start
```

O `npm start` inicia o servidor local para visualizar a aplicação no navegador. 

### 📂 Estrutura básica

Algumas pastas e arquivos importantes apresentados:

* **`node_modules/`** → pacotes e dependências instaladas;
* **`public/`** → arquivos públicos, como HTML, JSON e imagens;
* **`src/`** → código React da aplicação;
* **`.gitignore`** → define arquivos e diretórios ignorados pelo Git;
* **`package.json`** → configurações e dependências do projeto;
* **`package-lock.json`** → informações das dependências instaladas. 

Dentro da aplicação também aparecem arquivos como:

```text
index.js   → ponto de entrada do React
App.js     → componente principal
App.css    → estilos do componente App
index.css  → estilos globais
```



---

## 🚀 Deploy

**Deploy** é o processo de colocar uma aplicação em produção, tornando-a acessível aos usuários.

Normalmente envolve:

1. Compilação do código;
2. Configuração do ambiente;
3. Testes finais;
4. Publicação. 

---

## ▲ Vercel

A **Vercel** foi apresentada como plataforma para realizar o **deploy e hospedagem** de aplicações web.

Ela pode ser integrada ao GitHub, GitLab ou Bitbucket e realizar novos deploys automaticamente quando alterações são enviadas ao repositório.

Também oferece recursos como:

* Deploy automático;
* Rollback;
* Suporte a React e outros frameworks;
* Serverless Functions;
* CDN global;
* Escalabilidade e foco em performance. 

---

## 🛠️ Atividade Prática

A atividade proposta reúne os conceitos estudados na aula:

```text
Desenvolver aplicação React
        ↓
Utilizar VS Code
        ↓
Versionar com Git
        ↓
Commit + Push
        ↓
Publicar no GitHub
        ↓
Conectar com a Vercel
        ↓
Realizar o Deploy
        ↓
Aplicação disponível online
```

Ou seja, a atividade coloca em prática o fluxo completo de desenvolvimento, desde a criação do projeto até sua publicação na internet. 

---

## 📝 Resumo Geral

A **Aula 02** apresentou a preparação do ambiente necessário para o desenvolvimento Front-end. O foco principal foi entender a importância do **versionamento**, utilizar **Git** para controlar alterações no código, configurar o **VS Code**, instalar **Node.js e NPM**, compreender a estrutura básica de um projeto **React** e, por fim, realizar o **deploy da aplicação utilizando a Vercel**.

Essas ferramentas formam um fluxo básico de desenvolvimento moderno:

**VS Code → React → Git → GitHub → Vercel 🚀**
