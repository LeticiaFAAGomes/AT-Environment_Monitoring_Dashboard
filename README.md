# 🌱 Environment Monitoring Dashboard

### Aplicação Web para Monitoramento de Ambientes e Sensores

[![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
[![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/CSS)

Aplicação web desenvolvida em **React** para monitoramento e gerenciamento de ambientes e sensores, oferecendo uma interface centralizada para visualização de informações, favoritos, filtros, ordenação e acompanhamento dos dados de monitoramento.

---

## 💡 Sobre o Projeto

O **Environment Monitoring Dashboard** é uma aplicação web desenvolvida com **React** para auxiliar no acompanhamento de ambientes e sensores de monitoramento.

A aplicação apresenta um **dashboard centralizado**, permitindo visualizar ambientes cadastrados, consultar detalhes de localização, acompanhar sensores e realizar ações relacionadas ao monitoramento.

A interface foi organizada utilizando componentes reutilizáveis, separando as diferentes responsabilidades da aplicação.

---

## 🚀 Funcionalidades

### 🌎 Ambientes

- Listagem de ambientes
- Visualização de ambientes em cards
- Consulta de detalhes de localização
- Organização das informações dos ambientes

### 📡 Sensores

- Visualização dos sensores de monitoramento
- Cadastro de sensores
- Formulário para configuração de monitoramento
- Organização dos sensores por ambiente

### ⭐ Favoritos

- Visualização dos ambientes ou informações marcadas como favoritas
- Acesso separado aos itens favoritos

### 🔎 Filtros

- Filtragem dos ambientes
- Barra de filtros
- Controles de ordenação dos resultados

### 📊 Dashboard

- Visualização centralizada das informações
- Organização dos ambientes
- Acompanhamento dos sensores
- Controles de filtro e ordenação
- Acesso às funcionalidades de monitoramento

---

## 🏛️ Arquitetura

A aplicação utiliza uma organização baseada em **componentização React**, separando a página principal dos componentes responsáveis pelas diferentes funcionalidades.

```text
┌─────────────────────────────────────────────┐
│                   USUÁRIO                   │
└─────────────────────┬───────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────┐
│                    REACT                    │
│                                             │
│  ┌───────────────────────────────────────┐  │
│  │              Dashboard                │  │
│  │          Página principal             │  │
│  └───────────────────┬───────────────────┘  │
│                      │                      │
│       ┌──────────────┼──────────────┐       │
│       ▼              ▼              ▼       │
│   Environment      Filter         Sort      │
│      List           Bar         Controls    │
│       │                                     │
│       ▼                                     │
│   Environment                               │
│      Card                                   │
│       │                                     │
│       ├───────────────┐                     │
│       ▼               ▼                     │
│  Location Details   Sensors                 │
│                       │                     │
│              ┌────────┴────────┐            │
│              ▼                 ▼            │
│      Monitoring Form   Sensor Form          │
└─────────────────────────────────────────────┘
````

---

## 🛠️ Tecnologias

| Tecnologia     | Utilização                    |
| -------------- | ----------------------------- |
| **React**      | Desenvolvimento da interface  |
| **JavaScript** | Linguagem principal           |
| **CSS**        | Estilização da aplicação      |
| **HTML5**      | Estrutura da aplicação        |
| **npm**        | Gerenciamento de dependências |

---

## 📁 Estrutura do Projeto

```text
environment-monitoring/
│
├── public/
│   ├── api/
│   ├── favicon.ico
│   └── index.html
│
├── src/
│   │
│   ├── assets/
│   │   ├── css/
│   │   └── img/
│   │
│   ├── components/
│   │   │
│   │   ├── environmentCard/
│   │   ├── environmentList/
│   │   ├── favoritosView/
│   │   ├── filterBar/
│   │   ├── header/
│   │   ├── locationDetails/
│   │   ├── monitoringForm/
│   │   ├── monitoringSensorForm/
│   │   ├── monitoringSensors/
│   │   └── sortControls/
│   │
│   ├── pages/
│   │   └── Dashboard.jsx
│   │
│   ├── App.jsx
│   └── index.js
│
├── .gitignore
├── package.json
└── package-lock.json
```

---

## 🧩 Componentes

A aplicação é dividida em componentes independentes, facilitando a manutenção e reutilização do código.

### 🌎 EnvironmentCard

Responsável pela apresentação das informações de um ambiente em formato de card.

### 📋 EnvironmentList

Responsável pela organização e exibição da lista de ambientes.

### ⭐ FavoritosView

Apresenta os ambientes ou itens marcados como favoritos.

### 🔎 FilterBar

Disponibiliza os controles utilizados para filtrar os ambientes apresentados no dashboard.

### 🧭 Header

Responsável pela estrutura do cabeçalho da aplicação.

### 📍 LocationDetails

Apresenta informações relacionadas à localização de um ambiente.

### 📊 MonitoringForm

Componente destinado às configurações ou informações gerais de monitoramento.

### 📡 MonitoringSensorForm

Responsável pelo formulário relacionado ao cadastro ou configuração de sensores de monitoramento.

### 📡 MonitoringSensors

Responsável pela apresentação dos sensores associados aos ambientes.

### ↕️ SortControls

Disponibiliza controles para ordenação dos ambientes ou informações apresentadas.

---

## 📊 Dashboard

A página principal da aplicação está localizada em:

```text
src/pages/Dashboard.jsx
```

O **Dashboard** funciona como o ponto central da aplicação, reunindo os principais componentes de monitoramento:

```text
Dashboard
│
├── Header
│
├── FilterBar
├── SortControls
│
├── EnvironmentList
│   └── EnvironmentCard
│
├── LocationDetails
│
├── MonitoringSensors
│   └── MonitoringSensorForm
│
├── MonitoringForm
│
└── FavoritosView
```

Essa estrutura permite que as diferentes funcionalidades sejam apresentadas de forma organizada e independente.

---

## 🗂️ Organização dos Componentes

A separação dos componentes segue uma organização por responsabilidade:

```text
components/
│
├── Ambientes
│   ├── environmentCard
│   └── environmentList
│
├── Navegação
│   └── header
│
├── Filtros
│   ├── filterBar
│   └── sortControls
│
├── Favoritos
│   └── favoritosView
│
├── Localização
│   └── locationDetails
│
└── Monitoramento
    ├── monitoringForm
    ├── monitoringSensorForm
    └── monitoringSensors
```

Essa divisão facilita a evolução da aplicação e permite que cada funcionalidade seja desenvolvida de maneira independente.

---

## 🎨 Assets

Os recursos visuais e arquivos de estilização estão organizados dentro da pasta `assets`.

```text
assets/
├── css/
└── img/
```

A pasta `css` concentra os arquivos relacionados à aparência da aplicação, enquanto `img` contém os recursos gráficos utilizados na interface.

---

## 🚀 Como Executar

### Pré-requisitos

Antes de executar o projeto, é necessário possuir:

* Node.js
* npm

### 1. Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/environment-monitoring.git
```

### 2. Entre na pasta do projeto

```bash
cd environment-monitoring
```

### 3. Instale as dependências

```bash
npm install
```

### 4. Execute a aplicação

```bash
npm start
```

A aplicação será iniciada em modo de desenvolvimento e poderá ser acessada pelo endereço apresentado no terminal, normalmente:

```text
http://localhost:3000
```

---

## 📦 Scripts Disponíveis

### `npm start`

Executa a aplicação em modo de desenvolvimento.

### `npm test`

Executa os testes configurados no projeto.

### `npm run build`

Gera uma versão otimizada da aplicação para produção.

---

## 👩‍💻 Autora

**Letícia Gomes**

Projeto desenvolvido com fins acadêmicos para a disciplina de **Fundamentos de React**, aplicando conceitos de desenvolvimento de aplicações web com **React**, componentização, organização de interfaces e gerenciamento de informações de ambientes e sensores.
