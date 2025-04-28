## Instalando

# Na pasta root executar o commando a seguir

Passo 1
```shell
npm init -y
```

Passo 2
```shell
npm i -D typescript ts-node nodemon
```

# Passo 2 | Criar pasta src no root 
    - Crie uma pasta src na raiz
    - Dentro da pasta src crie um arquivo server.ts

# Passo 3 | Instalar JsonServer
    - npm i json-server@0.17.4

# Passo 4 | Tipos Typescript
    - npm i -D @types/json-server

# Instalação FEITA!!!

# Criar arquivo no root 
    - Crie um arquivo db.json
    - Digite o texto:
    ```json
    {
        "users": [],
        "products": []
    }
    ```
    - Salve o arquivo e inicialize com o commando a seguir:
    - npx json-server db.json