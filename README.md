# config-eslint-prettier-ts

Repositório para salvar configurações do **Eslint** + **Prettier** com *TypeScript*.

- Iniciar o projeto com:

```shell
npm init -y
```

```shell
npm install typescript @types/node
```

```shell
npx tsc --init
```

```shell
npm install -D tsx
```

- Instalar as dependências necessárias:

```shell
npm install --save-dev eslint-plugin-prettier eslint-config-prettier
```

```shell
npm install --save-dev --save-exact prettier
```

---

- Após instalar as dependências é necessário instalar e configurar o Eslint.

```shell
npm init @eslint/config@latest
```

- Cole esse código no arquivo `eslint.config.mjs`:
```js
import eslintPluginPrettierRecommended from 'eslint-plugin-prettier/recommended';

export default [
  // any other config imports go at the top
  eslintPluginPrettierRecommended
]
```

- Copie as configurações do arquivo [tsconfig.json](https://github.com/estanho/config-eslint-prettier-ts/blob/main/tsconfig.json)

---

### Bibliotecas interessantes:

- eslint-plugin-simple-import-sort
