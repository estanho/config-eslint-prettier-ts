# config-eslint-prettier-ts

Repositório para salvar configurações do **Eslint** + **Prettier** com *TypeScript*.

- Iniciar o projeto com:

```shell
npm init
```

```shell
npm install typescript @types/node -D
```

```shell
npx tsc --init 
```

```shell
npm install tsx -D # Node 22 roda com o Typescript
```

- Instalar as dependências necessárias:

```shell
npm install eslint eslint-config-prettier eslint-plugin-prettier @ianvs/prettier-plugin-sort-imports @eslint/js typescript-eslint -D
```

```shell
npm install prettier -D
```

---

- Após instalar as dependências é necessário configurar o Eslint.

```shell
npm init @eslint/config@latest
```

- Cole esse código no arquivo `eslint.config.mjs`:
```js
...
import eslintPluginPrettierRecommended from 'eslint-plugin-prettier/recommended';

export default [
  // Verificar se não existe outras configurações conflitando
  eslintPluginPrettierRecommended,
];
```

- Copie as configurações do arquivo [tsconfig.json](https://github.com/estanho/config-eslint-prettier-ts/blob/main/tsconfig.json)

---

- Para funcionar o autocomplete das variáveis de ambiente é necessário criar o arquivo chamado [environment.d.ts](https://github.com/estanho/config-eslint-prettier-ts/blob/main/environment.d.ts) e difinir as variáveis.

package.json:
```json
"scripts": {
  "dev": "tsx watch --env-file=.env server.ts"
},
```

---

### Bibliotecas interessantes:

- **cross-env**: para definir variáveis de ambiente sem erros em diferentes ambientes.
  - Instalar: `npm install cross-env -D`
  <br>

- **npm-run-all**: executar vários scripts em uma única linha.
  - Instalar: `npm install npm-run-all -D`
  <br>

- **tsup**: converte os arquivos `TS` em `JS` criando o *.dist/*.
  - Instalar: `npm install tsup -D`
  <br>

- **prisma-dbml-generator**: gera um arquivo que possibilita visualizar o banco de dados em um diagrama.
  - Instalar: `npm install prisma-dbml-generator -D`
  <br>

- **prisma**: um bom ORM :D
  - Instalar: `npm install prisma -D`
  <br>

  **pino-pretty**: deixa o logger *pino* mais bonito visualmente e fácil de entender (*pino é usado no fastify*).
    - Instalar: `npm install pino-pretty -D`
    <br>