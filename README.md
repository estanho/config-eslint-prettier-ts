# config-eslint-prettier-ts

Repositório para salvar configurações do **Eslint** + **Prettier** com *TypeScript*.

- Iniciar o projeto com:

```shell
pnpm init
```

```shell
pnpm install typescript @types/node -D
```

```shell
npx tsc --init
```

```shell
pnpm install tsx -D
```

- Instalar as dependências necessárias:

```shell
pnpm install eslint eslint-config-prettier eslint-plugin-prettier eslint-plugin-simple-import-sort @eslint/js typescript-eslint -D
```

```shell
pnpm install prettier -D
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
  // any other config imports go at the top
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

- **tsup**: converte os arquivos `TS` em `JS` criando o *.dist/*.
  - Instalar: `pnpm install tsup -D`
  <br>

- **prisma-dbml-generator**: gera um arquivo que possibilita visualizar o banco de dados em um diagrama.
  - Instalar: `pnpm install prisma-dbml-generator -D`
  <br>

- **prisma**: um bom ORM :D
  - Instalar: `pnpm install prisma -D`
  <br>

  **pino-pretty**: deixa o logger *pino* mais bonito visualmente e fácil de entender (*pino é usado no fastify*).
    - Instalar: `pnpm install pino-pretty -D`
    <br>