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