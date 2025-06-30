# 🧮 Desafio Técnico Fullstack — Análise Avançada de Sequências Numéricas (PHP + Vue)

## 📋 Descrição

Neste desafio, você deve desenvolver uma aplicação composta por back-end em **PHP** e front-end em **Vue**, capaz de analisar múltiplas sequências numéricas fornecidas pelo usuário e retornar uma análise detalhada de cada sequência.

A proposta deste desafio é avaliar sua capacidade de estruturar algoritmos, lidar com restrições técnicas e desenvolver soluções limpas, eficientes e bem documentadas.

---

## 🎯 Objetivo

Receber uma string contendo várias sequências numéricas separadas por ponto e vírgula (`;`), normalizar os dados e, para cada sequência, realizar as seguintes análises:

- Se é **estritamente crescente**
- Se é **estritamente decrescente**
- Se possui **números repetidos**
- Se todos os dígitos são **ímpares**, **pares** ou **misto**
- Se a soma dos dígitos é **divisível por 3**

A resposta deve ser retornada como um array de objetos JSON, cada um contendo as análises realizadas.

---

## 🚦 Regras & Restrições

- 🚫 **Não é permitido utilizar funções nativas de manipulação de strings do PHP** (ex: `str_replace`, `substr`, `strlen`, `str_pad`, `preg_match`, `preg_replace`, etc.).
- 🚫 **Você pode utilizar apenas UMA ÚNICA VEZ qualquer função nativa de string do PHP** (à sua escolha, em qualquer parte do código).
- ✅ Laços de repetição (`for`, `foreach`, `while`), estruturas condicionais (`if`, `switch`), funções (`isset`) e arrays estão permitidos.
- ✅ O front-end deve ser simples e funcional, focando apenas na usabilidade do desafio.
- ✅ O input do usuário NÃO pode ter máscara, só números e separador ponto e vírgula.

---

## 🖥️ Estrutura Esperada

### **Back-end (PHP)**
- Rota que recebe a string via POST.
- Processa as sequências conforme as regras.
- Retorna a resposta em JSON.

### **Front-end (Vue)**
- Campo para digitar as sequências (ex: `12345; 9889; 112211; 1243; 321; 13579; 2468`).
- Botão para enviar.
- Exibição do resultado em formato organizado.

---

## 🔎 Exemplo de Entrada e Saída

**Entrada do usuário:** 12345; 9889; 112211; 1243; 321; 13579; 2468

**Resposta esperada (JSON):**
```json
[
  {
    "sequencia": "12345",
    "crescente": true,
    "decrescente": false,
    "repetidos": false,
    "digitos": "misto",
    "soma_divisivel_por_3": true
  },
  {
    "sequencia": "9889",
    "crescente": false,
    "decrescente": false,
    "repetidos": true,
    "digitos": "misto",
    "soma_divisivel_por_3": false
  },
  {
    "sequencia": "112211",
    "crescente": false,
    "decrescente": false,
    "repetidos": true,
    "digitos": "misto",
    "soma_divisivel_por_3": true
  },
  {
    "sequencia": "1243",
    "crescente": false,
    "decrescente": false,
    "repetidos": false,
    "digitos": "misto",
    "soma_divisivel_por_3": false
  },
  {
    "sequencia": "321",
    "crescente": false,
    "decrescente": true,
    "repetidos": false,
    "digitos": "misto",
    "soma_divisivel_por_3": false
  },
  {
    "sequencia": "13579",
    "crescente": true,
    "decrescente": false,
    "repetidos": false,
    "digitos": "ímpares",
    "soma_divisivel_por_3": false
  },
  {
    "sequencia": "2468",
    "crescente": true,
    "decrescente": false,
    "repetidos": false,
    "digitos": "pares",
    "soma_divisivel_por_3": false
  }
]
```
