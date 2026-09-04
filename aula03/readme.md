# 📚 Aula 03 — Projetos com Frameworks Front-end

Nesta aula foram apresentados os principais conceitos relacionados aos **frameworks Front-end**, suas características, diferenças em relação às bibliotecas e a utilização de tecnologias como **React, Angular, Vue e Next.js**. Também foram abordadas a criação e estruturação de projetos, reutilização de projetos existentes e versionamento com Git. 

---

## 🧩 O que são Frameworks Front-end?

Um **framework Front-end** é um conjunto de ferramentas, bibliotecas e convenções que fornece uma estrutura para desenvolver interfaces Web.

Comparando com o desenvolvimento utilizando apenas JavaScript (**Vanilla JS**):

* **Sem framework:** maior quantidade de código manual, repetição e manutenção mais difícil;
* **Com framework:** utilização de componentes reutilizáveis, gerenciamento de estado e atualizações mais eficientes da interface. 

---

## 📚 Framework x Biblioteca

Apesar de serem conceitos semelhantes, **frameworks e bibliotecas possuem diferenças importantes**.

### 🏗️ Framework

O framework define uma estrutura que deve ser seguida e possui maior controle sobre o fluxo da aplicação.

**Exemplos apresentados:**

* Angular
* Vue

### 📦 Biblioteca

Uma biblioteca oferece funcionalidades que podem ser utilizadas quando o desenvolvedor precisar, oferecendo maior liberdade sobre a estrutura da aplicação.

**Exemplos apresentados:**

* React
* jQuery

A principal diferença está no **controle da aplicação**: em uma biblioteca, o desenvolvedor decide quando utilizar seus recursos; em um framework, a própria estrutura do framework determina parte do funcionamento. 

---

## 🚀 Por que utilizar Frameworks?

Frameworks e ferramentas semelhantes facilitam o desenvolvimento de aplicações mais complexas.

Entre os principais benefícios estão:

* ⚡ **Maior produtividade** — soluções prontas evitam desenvolver tudo do zero;
* 🧱 **Organização** — código dividido em componentes;
* 🔧 **Facilidade de manutenção**;
* ♻️ **Reutilização de código**;
* 📚 **Comunidade e documentação**;
* 🔌 **Integração com APIs**;
* 🧪 **Suporte a testes**;
* 🛣️ **Sistemas de rotas para SPAs**.  

---

## 🧱 Componentização

Uma característica importante do desenvolvimento Front-end moderno é a **componentização**.

Um componente representa uma parte independente e reutilizável da interface. Dessa forma, elementos como:

```text
Header
Navbar
Button
Card
Footer
```

podem ser desenvolvidos separadamente e reutilizados em diferentes partes da aplicação.

Isso facilita a **organização, manutenção e evolução do código**. 

---

# ⚛️ React

O **React** é uma biblioteca JavaScript utilizada para desenvolver interfaces de usuário e aplicações Web.

Sua arquitetura é baseada em **componentes reutilizáveis** e utiliza o **Virtual DOM**, permitindo a criação de aplicações rápidas e escaláveis. 

### 🪝 Conceitos importantes

Entre os conceitos apresentados estão os **Hooks**:

* `useState` → gerencia o estado de um componente;
* `useEffect` → utilizado para efeitos colaterais, como chamadas de APIs.

Também foi apresentado o **JSX**, que permite combinar elementos semelhantes ao HTML com JavaScript.

Exemplo:

```jsx
const nome = "Guilherme";

function App() {
  return <h1>Olá, {nome}!</h1>;
}
```

No JSX:

```text
{}        → permite utilizar expressões JavaScript
className → utilizado no lugar de class
<img />   → as tags precisam ser fechadas
```

Para gerenciamento de estado, também foram citados **Context API** para situações mais simples e **Redux** para estados mais complexos e compartilhados. 

---

## 🌳 DOM e Virtual DOM

O **DOM (Document Object Model)** representa a estrutura de uma página Web como uma árvore que pode ser manipulada pelo JavaScript.

O React utiliza o **Virtual DOM**, uma representação do DOM. Quando ocorre alguma alteração, o React compara o Virtual DOM com o DOM real e aplica somente as diferenças necessárias, buscando tornar as atualizações mais eficientes. 

---

# 🅰️ Angular

O **Angular** é um framework completo voltado ao desenvolvimento de aplicações Web, principalmente **Single Page Applications (SPAs)**.

Entre seus principais recursos estão:

* TypeScript;
* Roteamento;
* HTTP Client;
* Injeção de dependências;
* Arquitetura organizada;
* Angular CLI;
* Change Detection. 

### 🧩 Conceitos do Angular

A aula apresentou:

* **Components** → componentes da aplicação;
* **Modules** → organização em blocos funcionais;
* **Services** → lógica reutilizável;
* **Data Binding** → ligação entre dados e interface;
* **Dependency Injection** → gerenciamento de dependências;
* **RouterModule** → navegação entre páginas/views. 

### 💻 Criando um projeto Angular

Primeiro, instala-se o Angular CLI:

```bash
npm install -g @angular/cli
```

Depois:

```bash
ng new meu-app-angular
cd meu-app-angular
code .
ng serve
```

O **Angular CLI** facilita a criação, gerenciamento e construção de projetos Angular. 

---

# 🟢 Vue.js

O **Vue** é apresentado como um framework progressivo, podendo ser utilizado tanto em partes menores de uma aplicação quanto em projetos maiores e SPAs.

Entre suas características estão:

* ⚡ Sistema de reatividade;
* 🧩 Desenvolvimento baseado em componentes;
* 📄 **Single-File Components (SFC)**;
* 📚 Curva de aprendizado mais suave;
* 🚀 Virtual DOM e foco em performance. 

### 💻 Criando um projeto Vue

```bash
npm create vue@latest
```

Depois:

```bash
cd meu-projeto-vue
npm install
code .
npm run dev
```



### 📂 Estrutura do Vue

Entre os principais arquivos e diretórios:

```text
src/
├── assets/
├── components/
├── App.vue
└── main.js

public/
index.html
package.json
vite.config.js
.gitignore
```

* **`assets/`** → imagens, fontes, CSS etc.;
* **`components/`** → componentes reutilizáveis;
* **`App.vue`** → componente raiz;
* **`main.js`** → ponto de entrada da aplicação;
* **`index.html`** → HTML principal da SPA. 

---

# ▲ Next.js

O **Next.js** é um framework baseado em React voltado para aplicações Web modernas e **full-stack**.

Ele adiciona diversos recursos que não fazem parte diretamente do React, como:

* 🛣️ Roteamento baseado em arquivos;
* 🖥️ Renderização no servidor;
* 🧩 Server Components;
* 🖼️ Otimização de imagens e fontes;
* 📄 Gerenciamento de páginas e layouts;
* ⚙️ APIs e recursos de backend;
* 🔎 Otimizações de desempenho e SEO. 

### 💻 Criando um projeto Next.js

```bash
npx create-next-app@latest meu-projeto
```

Depois:

```bash
cd meu-projeto
code .
npm run dev
```



### 📂 App Router

No Next.js, a pasta **`app/`** pode armazenar páginas, layouts, estilos e outros componentes da aplicação.

A estrutura das pastas é utilizada para definir as **rotas**, enquanto arquivos como `page.js` representam páginas da aplicação. 

---

# ⚖️ Comparação das Tecnologias

A aula reforça que não existe uma única tecnologia ideal para todos os projetos. A escolha deve considerar fatores como **complexidade, curva de aprendizado, desempenho, escalabilidade e suporte da comunidade**. 

| Tecnologia      | Tipo                       | Principal característica                          |
| --------------- | -------------------------- | ------------------------------------------------- |
| **React** ⚛️    | Biblioteca                 | Componentes e Virtual DOM                         |
| **Angular** 🅰️ | Framework                  | Estrutura completa e TypeScript                   |
| **Vue** 🟢      | Framework progressivo      | Simplicidade e reatividade                        |
| **Next.js** ▲   | Framework baseado em React | Full-stack, roteamento e renderização no servidor |

---

# 📥 Importando Projetos

Também foi apresentado que nem sempre é necessário desenvolver uma aplicação completamente do zero.

É possível utilizar projetos e templates **open source** como ponto de partida, estudando e personalizando estruturas existentes.

Entre as ferramentas citadas estão:

* **GitHub** → pesquisa de repositórios;
* **Vercel** → templates;
* **CodeSandbox** → pesquisa de templates. 

Para copiar um repositório Git:

```bash
git clone <url>
```

---

# 🌿 Git e Versionamento dos Projetos

Os projetos desenvolvidos durante a atividade devem utilizar **Git** para registrar sua evolução e ser publicados no **GitHub**.

O objetivo é manter um histórico de commits mostrando as mudanças realizadas durante o desenvolvimento. 

Um fluxo básico seria:

```text
Criar/alterar projeto
        ↓
git add .
        ↓
git commit
        ↓
git push
        ↓
GitHub
```

---

# 🛠️ Atividade Prática

A atividade proposta consiste em desenvolver **quatro projetos Web sobre o mesmo tema**, utilizando:

```text
Projeto 01 → React ⚛️
Projeto 02 → Vue 🟢
Projeto 03 → Angular 🅰️
Projeto 04 → Next.js ▲
```

Cada projeto deve possuir uma página **funcional, responsiva e organizada**, utilizando componentes e recursos básicos da tecnologia escolhida. 

Além desses projetos, também deverá ser entregue:

```text
Projeto 05 → Cópia de um projeto a partir de um repositório
```



Ao final, deve ser feita uma comparação entre as quatro tecnologias, destacando as principais diferenças percebidas durante o desenvolvimento.

---

# 📝 Resumo Geral

A **Aula 03** aprofundou o estudo sobre **Frameworks Front-end**, mostrando como essas ferramentas ajudam a criar aplicações mais organizadas, reutilizáveis e fáceis de manter.

Foram estudadas quatro tecnologias principais:

**React ⚛️ → Angular 🅰️ → Vue 🟢 → Next.js ▲**

Além dos conceitos de cada tecnologia, a aula mostrou **como criar e estruturar projetos**, trabalhar com **componentes**, compreender conceitos como **DOM, Virtual DOM e reatividade**, aproveitar projetos existentes e utilizar **Git e GitHub** para versionar o desenvolvimento.

De forma geral, o fluxo trabalhado na aula pode ser resumido como:

**Escolher a tecnologia → Criar o projeto → Desenvolver com componentes → Versionar com Git → Publicar no GitHub → Comparar as tecnologias 🚀**
