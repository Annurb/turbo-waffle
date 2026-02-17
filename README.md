# turbo-waffle

Um projeto full-stack para treinar programação

## Configuração do ambiente de desenvolvimento

Para instalar a versão correta do node, usamos o comando para retornar as versões disponíveis do node:

```bash
nvm ls
```

Depois a versão atualizada foi lts/hydrogen:

```bash
nvm install lts/hydrogen
```

Ao executar:

```bash
node -v
```

A versão do lts é atualizada

Porém, para colocar como padrão, já que ele não padroniza automaticamente:
Ao executar:

```bash
nvm --help
```

Em exemplos, copiamos o código e adicionamos a versão padrão:

```bash
nvm alias default lts/hydrogen
```

E, após criar o arquivo .nvmrc, atualizamos com a versão e rodamos:

```bash
nvm install
```

**Criação do package.json:**

```bash
npm init
```

**Instalação do next.js:**

```bash
npm install next@13.1.6
```

**Instalação do react.js:**

```bash
npm install react@18.2.0 react-dom@18.2.0
```

## Deploy:

O deploy inicial do site foi feito pelo Vercel através de sua conexão com o github ao logar.

Link do site:

https://turbo-waffle.vercel.app/
