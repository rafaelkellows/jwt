# Instalando do ZERO

## Na pasta root do projeto execute o commando a seguir:

```shell
npm init -y
```

Após isso, execute o commando a seguir:

```shell
npm i -D typescript ts-node nodemon
```

## Crie a pasta src no root do projeto
- Crie uma pasta src na raiz
- Dentro da pasta src crie um arquivo server.ts

## | Instale o JsonServer
```shell
npm i json-server@0.17.4
```

## | Instale Tipos Typescript
```shell
npm i -D @types/json-server
```

### Instalação FEITA!!!

## Crie arquivo no root 
- Crie um arquivo db.json e inclua:

```json
{
    "users": [],
    "products": []
}
```
- Salve o arquivo e inicialize com o commando a seguir:
```shell
npx json-server db.json
```

## Crie um tsconfig.json com o commando:

```shell
npx tsc --init
```
- No arquivo mudar a referencia "target" de "es2016" para "ES2022"
- Descomente "outDir" e coloque o diretorio do build do projeto como "./dist"

## Altera o arquivo server.js.

```js
import jsonServer from "json-server";

const databasePath = "db.json"

const server = jsonServer.create()
const router = jsonServer.router(databasePath)

server.use(jsonServer.defaults({
    bodyParser: true
}))

server.post('/register',(req, res) => {
    return res.json("Tudo ok!")
})

server.use(router)

server.listen(3000, () => {
    console.log("Server ruuning!")
})
```

## Criar script no pachage.json (ou substituir a tag test) 
```json
"scripts": {
    "dev": "nodemon --exec ts-node ./src/server.ts"
  },
```
- Execute a seguir:
```shell
npm run dev
```
Teste no POSTMAN