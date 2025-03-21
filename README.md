# Configurando um Projeto Node.js Básico

Este guia explica como configurar um projeto Node.js básico, criando uma estrutura de pastas, inicializando o `package.json`, e configurando um servidor HTTP simples.

---

## Passos para Configuração

### 1. Criar uma Pasta para o Projeto
Use no terminal o comando `mkdir` para criar uma pasta chamada `fundamentos-nodejs`:
```bash
mkdir fundamentos-nodejs
```
### 2. Entrar na Pasta do Projeto
Navegue para a pasta criada:
```bash
cd fundamentos-nodejs
```

### 3. Inicializar o Projeto Node.js
Use o comando `npm init -y` para criar o arquivo `package.json` com configurações padrão:
```bash
npm init -y
```
**Explicação**:
- O comando `npm init -y` cria um arquivo `package.json` automaticamente, respondendo "sim" a todas as perguntas.

### 4. Criar a Pasta `src`
Crie uma pasta chamada `src` para armazenar o código-fonte do projeto:
```bash
mkdir src
```

**Explicação**:
- A pasta `src` (abreviação de "source") é uma convenção comum para armazenar arquivos de código-fonte.

### 5. Entrar na Pasta `src`
Navegue para a pasta `src`:
```bash
cd src
```

## 6. Criar um Arquivo `server.js`
Crie um arquivo chamado `server.js` dentro da pasta `src`:
```bash
touch server.js
```
**Explicação**:
- O arquivo `server.js` será o ponto de entrada do seu servidor Node.js.

# Configurando `"type": "module"` no `package.json`

Para usar **ES Modules** (sintaxe `import`/`export`) no Node.js, você precisa configurar o campo `"type": "module"` no arquivo `package.json`. Isso permite que o Node.js interprete os arquivos `.js` como módulos ES por padrão.

---

## Passos para Configurar

1. Abra o arquivo `package.json` no seu projeto.
2. Adicione a linha `"type": "module"` no objeto principal.

Exemplo de `package.json` configurado:

```json
{
  "name": "nodejs",
  "type": "module",  // Habilita ES Modules
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": ""
}
```
### O Que Isso Faz?

- **`"type": "module"`**: Define que todos os arquivos `.js` no projeto devem ser tratados como módulos ES (ECMAScript Modules).
- Com isso, você pode usar a sintaxe `import`/`export` em vez de `require`/`module.exports`.

## Exemplo de Uso

```javascript

import http from 'node:http';

