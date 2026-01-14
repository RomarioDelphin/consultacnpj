<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=250&section=header&text=CNPJ%20INTELLIGENCE&fontSize=60&fontAlignY=35&desc=Data%20Mining%20Tool%20|%20Consulta%20Corporativa%20em%20Tempo%20Real&descAlignY=55&descSize=18&fontColor=ffffff&customColorList=06b6d4,000205&animation=fadeIn" width="100%"/>
</div>

<div align="center">
  <br />
  
  <a href="https://github.com/RomarioDelphin">
    <img src="https://img.shields.io/badge/DEV-ROMARIO%20DELPHIN-000205?style=for-the-badge&logo=github&logoColor=06b6d4&labelColor=000205&color=06b6d4" />
  </a>
  <img src="https://img.shields.io/badge/API-RECEITA%20WS-000205?style=for-the-badge&logo=postman&logoColor=FF6C37&labelColor=000205&color=FF6C37" />
  <img src="https://img.shields.io/badge/TECH-VANILLA%20JS-000205?style=for-the-badge&logo=javascript&logoColor=F7DF1E&labelColor=000205&color=F7DF1E" />

</div>

<br />

## ⚡ Sobre o Projeto

O **CNPJ Intelligence** é uma solução de *Data Retrieval* desenvolvida para consultar, em tempo real, dados públicos de empresas brasileiras.

A ferramenta atua como um **Client-Side Interface** para a API da ReceitaWS, permitindo que analistas e gestores verifiquem a saúde cadastral, quadro societário e dados fiscais de parceiros de negócios de forma instantânea, sem necessidade de softwares pesados.

### 🎯 Funcionalidades Core
* **🔍 Busca Precisa:** Validação de formato e input de CNPJ.
* **🌐 Tunneling via Proxy:** Solução técnica para contornar restrições de CORS (Cross-Origin Resource Sharing) utilizando *AllOrigins*.
* **📊 Visualização de Dados:** Cards informativos que organizam dados complexos (Natureza Jurídica, Sócios, Endereço) em UI limpa.
* **🛡️ Tratamento de Erros:** Feedback visual imediato para CNPJs inválidos ou falhas de conexão.

---

## 🛠️ Tech Stack & Arquitetura

O projeto segue o princípio "Less Dependencies", utilizando tecnologias nativas da web para máxima performance e compatibilidade.

<div align="center">
  <img src="https://skillicons.dev/icons?i=html,css,js&perline=10" />
</div>

| Camada | Tecnologia | Função |
| :--- | :--- | :--- |
| **Estrutura** | `HTML5` | Marcação semântica e acessível. |
| **Estilo** | `CSS3` | Design responsivo e cartões de dados. |
| **Lógica** | `JavaScript (ES6+)` | Manipulação do DOM, Regex para validação e Fetch API. |
| **Dados** | `ReceitaWS API` | Fonte dos dados corporativos. |

---

## 🧬 Detalhe Técnico: O Desafio do CORS

Para permitir que esta aplicação rode diretamente no navegador do cliente sem um Backend dedicado, implementou-se uma arquitetura de proxy:

```javascript
// O browser bloquearia a requisição direta à ReceitaWS por segurança (CORS).
// Solução: Encapsulamos a chamada através do proxy 'allorigins'.

const proxyUrl = '[https://api.allorigins.win/raw?url=](https://api.allorigins.win/raw?url=)';
const targetUrl = `https://www.receitaws.com.br/v1/cnpj/${cnpjLimpo}`;

// O fetch busca no proxy, que busca na Receita e devolve os dados limpos.
const response = await fetch(`${proxyUrl}${targetUrl}`);

```

---

## 🚀 Como Utilizar

Não é necessário instalação de dependências (npm/yarn). O projeto é *Plug & Play*.

### 1. Clone o Repositório

Baixe os arquivos para o seu ambiente local:

```bash
git clone [https://github.com/RomarioDelphin/consultacnpj.git](https://github.com/RomarioDelphin/consultacnpj.git)

```

### 2. Execute

* Navegue até a pasta do projeto.
* Abra o arquivo `index.html` em qualquer navegador moderno (Chrome, Edge, Firefox).

### 3. Operação

* Digite um CNPJ no campo de busca (ex: `00.000.000/0001-91`).
* Clique no botão **Consultar**.
* Analise os dados retornados no Card Corporativo.

---

<div align="center">
<p>Desenvolvido por <strong>Romário Delphin</strong> como parte do portfólio <strong>RAM.IO Holdings</strong>.</p>
</div>

```

```
