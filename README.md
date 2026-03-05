# turbo-waffle

Um projeto full-stack para treinar programação

---

### Menu:

- [Configuração do ambiente de desenvolvimento](#config)
- [Funcionalidades](#deploy)
- [Arquitetura de software](#arq)
- [Testes automatizados](#testes)
- [Subindo banco de dados local](#banco-local)
- [Subindo banco de Produção](#banco-producao)

---

## <a name="config"></a> Configuração do ambiente de desenvolvimento

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

---

## <a name="deploy"></a>Deploy:

O deploy do site foi feito pelo Vercel através de sua conexão com o github ao logar.

Link do site:

https://turbo-waffle.vercel.app/

O site também foi hospedado em `.com.br` pelo período de um ano através do link:

https://turbo-waffle.com.br/

## Arquitetura de software

---

## <a name="arq"></a>Arquitetura de software

Por padrão, a arquitetura de software utilizada será a MVC (Model-View-Controller)

---

## <a name="testes"></a>Testes automatizados

Os testes automatizados foram feitos usando a tecnologia Jest, escolhido com base em sua popularidade e facilidade de uso.

---

## <a name="banco-local"></a>Subindo Banco de Dados local

Para subir o banco de dados local foi utilizado o Docker compose, através do arquivo compose.yaml e o seguinte site postgres e comando:

https://hub.docker.com/_/postgres

```bash
docker compose up
```

---

## <a name="banco-producao"></a>Subindo Banco de Produção

A escolha do banco de dados de produção para esse projeto foi a Neon, um banco de dados relacional serveless, por sua disponibilidade e gratuidade. O ssl teve que ser configurado, e as variáveis de produção do banco atualizadas na Vercel.

### Migrations:

O uso de migrations foi usado para aplicar alterações no schema do banco de dados de forma automática e segura.

#### Arquivos de migração

Define ordem e alterções que vão ser feitas.

#### Framework de Migração

Garantir que vai ser executado na ordem e uma única vez.
O framework usado foi o node-pg-migrate, que executa focado no postgres e não em todos os bancos de dados, escolhendo foco ao invés de flexibilidade. Ele foi configurado através do site e códigos abaixo:

https://www.npmjs.com/package/node-pg-migrate

```bash
npm install node-pg-migrate@6.2.2
```

Para se conectar ao banco pelo comando `migration:up`, o dotenv precisou ser instalado também:

```bash
npm install dotenv@16.4.4
```
