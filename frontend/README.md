# config-eslint-prettier-ts

Repositório para salvar configurações do **Eslint** + **Prettier** com *TypeScript*.

- Instalar as dependências necessárias:

```shell
npm install eslint prettier prettier-plugin-tailwindcss eslint-config-prettier eslint-plugin-prettier @ianvs/prettier-plugin-sort-imports @eslint/js typescript-eslint -D
```

---

- Cole esse código no arquivo `eslint.config.mjs`:

```js
...
import eslintPluginPrettierRecommended from 'eslint-plugin-prettier/recommended';

export default [
  // Verificar se não existe outras configurações conflitando
  eslintPluginPrettierRecommended,
];
```

---

- Crie o arquivo `.prettierrc.json` com o seguinte conteúdo:

```json
{
  "trailingComma": "es5",
  "semi": true,
  "tabWidth": 2,
  
  "parserOptions": {
    "sourceType": "module",
    "ecmaVersion": "latest"
  },
  "plugins": ["@ianvs/prettier-plugin-sort-imports", "prettier-plugin-tailwindcss"],
  "importOrder": ["^@core/(.*)$", "", "^@server/(.*)$", "", "^@ui/(.*)$", "", "^[./]"],
  "importOrderParserPlugins": ["typescript", "jsx", "decorators-legacy"],
  "importOrderTypeScriptVersion": "5.0.0",
  "importOrderCaseSensitive": false
}
```