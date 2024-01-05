# 1. M1#A01 - Aula inaugural

- [Doc do React](https://react.dev/)

- [[JSConfUS 2013] Tom Occhino and Jordan Walke: JS Apps at Facebook](https://youtu.be/GW0rj4sNH2w?si=IebpQH3-4JpLoGtJ)

- Scripts para começar a testar React sem JSX:

```html
<script src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
```

- Script do Babel:

```html
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
```

- Snippets
  - [Doc do VSCode](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
  - [Meus Snippets](https://github.com/roger-melo-treinamentos/passo-a-passo-de-projetos-reactjs/blob/main/config/snippets/javascript.json)
  - [Snippet Generator](https://snippet-generator.app/)

---

# 3. M1#A03 - Resolução Bateria de Desafios 01 + Vite e Configuração do Ambiente

- [Como instalar o WSL no Windows](https://learn.microsoft.com/en-us/windows/wsl/install)
- [Node JS](https://nodejs.org/en)
- [NVM](https://github.com/nvm-sh/nvm)
- [Vite](https://vitejs.dev/)
- [Semantic Versioning](https://semver.org/)
- [NPM Docs](https://docs.npmjs.com/cli/v10)
- [ESLint](https://eslint.org/)
- [Prettier](https://prettier.io/)

---

# 4. M1#A04 - ES Modules

- [Importing and Exporting Components - React docs](https://react.dev/learn/importing-and-exporting-components)

---

# 5. M1#A05 - StrictMode e O jeito certo de renderizar listas e manipular eventos

<details>
<br />
<summary>CSS usado na Aula</summary>

```css
ul {
  list-style: none;
}

.game {
  margin-top: 50px;
}

.img-width {
  width: 100px;
}
```
</details>

<details>
<br />
<summary>Array usado na Aula</summary>

```js
const games = [
  {
    id: "61sM22Dx3uL",
    name: "Mortal Kombat 1",
    description: "Mortal Kombat 1 traz um novo mundo, criado pelo Guardião do Tempo e protetor do Plano Terreno, o Deus do Fogo Liu Kang.",
    price: 270,
    imgUrl: "https://m.media-amazon.com/images/I/61sM22Dx3uL._AC_SL1000_.jpg",
  },
  {
    id: "610aw15JvKL",
    name: `Assassin's Creed Mirage`,
    description: `Em Assassin's Creed Mirage, você é Basim, um astucioso ladino de rua em busca de respostas e de justiça.`,
    price: 257.68,
    imgUrl: "https://m.media-amazon.com/images/I/610aw15JvKL._AC_SL1000_.jpg",
  },
  {
    id: "61te8AW6zjL",
    name: "EA Sports FC 24",
    description: "O EA SPORTS FC 24 traz para você o Jogo de Todo Mundo.",
    price: 263.11,
    imgUrl: "https://m.media-amazon.com/images/I/61te8AW6zjL._AC_SL1020_.jpg",
  },
  {
    id: "711nB1PK-wL",
    name: "Super Mario Bros. Wonder",
    description: "Encante-se com a evolução fenomenal da diversão com o Mario.",
    price: 349,
    imgUrl: "https://m.media-amazon.com/images/I/711nB1PK-wL._AC_SL1276_.jpg",
  },
  {
    id: "81RfcW3Ml-L",
    name: `Marvel's Spider-Man 2`,
    description: `Peter Parker e Miles Morales retornam para uma nova e emocionante aventura na aclamada franquia de Marvel's Spider-Man.`,
    price: 296.91,
    imgUrl: "https://m.media-amazon.com/images/I/81RfcW3Ml-L._AC_SL1500_.jpg",
  },
  {
    id: "619mg6uGj-L",
    name: "Sonic Superstars",
    description: "Embarque numa jornada para as ilhas Northstar nessa novíssima versão clássica 2D de Sonic.",
    price: 269,
    imgUrl: "https://m.media-amazon.com/images/I/619mg6uGj-L._AC_SL1000_.jpg",
  },
]
```
</details>

### Listagem de eventos que podem ser usados no React

- [Handling mouse events](https://react.dev/reference/react-dom/components/common#handling-mouse-events)
- [Handling pointer events](https://react.dev/reference/react-dom/components/common#handling-pointer-events)
- [Handling focus events](https://react.dev/reference/react-dom/components/common#handling-focus-events)
- [Handling keyboard events](https://react.dev/reference/react-dom/components/common#handling-keyboard-events)

---

# 7. M1#A07 - Introdução a estado no React

<details>
<br />
<summary>JSX inicial da Aula</summary>

```jsx
const App = () => (
  <div>
    <h1>Contagem: 0</h1>
    <button>+</button>
  </div>
)

export { App }
```
</details>

<details>
<br />
<summary>CSS inicial da Aula</summary>

```css
div {
  display: flex;
  flex-direction: column;
  align-items: center;
}

button {
  width: 20%;
}
```
</details>

- [State: A Component's Memory](https://react.dev/learn/state-a-components-memory)
- [useState](https://react.dev/reference/react/useState)

---

# 8. M1#A08 - Introdução a estado no React - Parte 2

- [Queueing a Series of State Updates](https://react.dev/learn/queueing-a-series-of-state-updates)
- [Sharing State Between Components](https://react.dev/learn/sharing-state-between-components)

---

# 10. M1#A10 - Formulários controlados e não controlados

<details>
<br />
<summary>JSX e CSS iniciais do exemplo onSubmit</summary>

```css
label {
  display: block;
  margin: 20px 0;
}

select,
input {
  margin-left: 5px;
}
```

```jsx
const App = () => {
  const handleSubmit = (e) => {
    e.preventDefault()
    console.log(e.target)
  }

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Idade:
        <select>
          <option value="17">17 anos</option>
          <option value="18">18 anos</option>
          <option value="19">19 anos</option>
        </select>
      </label>

      <label>
        Nome da Mãe:
        <input placeholder="Escreve aqui" />
      </label>

      <button>Enviar</button>
    </form>
  )
}

export { App }
```
</details>

### Imutabilidade

- [Em Objetos](https://react.dev/learn/updating-objects-in-state)
- [Em Arrays](https://react.dev/learn/updating-arrays-in-state)

### Forms

- [A propriedade `elements`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/elements)
- Elementos importantes de forms no React:
  - [input](https://react.dev/reference/react-dom/components/input)
  - [select](https://react.dev/reference/react-dom/components/select)
  - [option](https://react.dev/reference/react-dom/components/option)

---

# 13. M1#A13 - Resetar form, estrutura de diretórios e próximo projeto

- [Queueing a Series of State Updates](https://react.dev/learn/queueing-a-series-of-state-updates)

---

# 16. M1#A16 - Lifecycle de um componente, Requests HTTP e hook useEffect

- [Keeping Components Pure](https://react.dev/learn/keeping-components-pure)
- [useEffect](https://react.dev/reference/react/useEffect)

---

# 20. M2#A02 - Atualização de dependências e Primeiras implementações da Bateria 09 (Me Avalia)

<details>
<br />
<summary>Comando para atualizar as dependências do vite-boilerplate</summary>

```
npm i --save-dev --save-exact @types/react@18.2.38 @types/react-dom@18.2.17 @vitejs/plugin-react@4.2.0 eslint@8.54.0 eslint-plugin-react@7.33.2 eslint-plugin-react-refresh@0.4.4 vite@5.0.2
```
</details>

---

# 22. M2#A04 - Hook useRef, hooks personalizados, imagens quebradas e reposicionamento de estado

- [Placeholder para imagens quebradas](assets/lessons/22/404-img.jpg)
- [useRef](https://react.dev/reference/react/useRef)
- [Ref x state](https://react.dev/learn/referencing-values-with-refs#differences-between-refs-and-state)

---

# 26. M2#A08 - Aliases no Vite e Hook useReducer

- [Extracting State Logic into a Reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)
- [useReducer](https://react.dev/reference/react/useReducer)

<details>
<br />
<summary>CSS e JSX iniciais do 1º exemplo</summary>

```css
h1 {
  font-size: 2.5rem;
  margin-bottom: .8rem;
}

div {
  text-align: center;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: .4rem;
}

.buttons button {
  padding: 10px 20px;
  font-size: 1rem;
}
```

```jsx
const App = () => {
  return (
    <div>
      <h1>Contagem: X</h1>
      <div className="buttons">
        <button>-</button>
        <button>+</button>
        <button>Reset</button>
      </div>
    </div>
  )
}

export { App }
```

</details>

---

# 28. M2#A10 - Atualização de Dependências do vite-boilerplate e Apresentação do Próximo Projeto

<details>
<br />
<summary>Atualização de dependências com versões exatas</summary>

```
npm i --save-dev --save-exact @types/react@18.2.43 @vitejs/plugin-react@4.2.1 eslint@8.55.0 eslint-plugin-react-refresh@0.4.5 vite@5.0.7
```

</details>

---

# 31. M2#A13 - Delay em Timer, Dependências do useEffect, Memoização e Introdução ao Hook useCallback

- [useCallback](https://react.dev/reference/react/useCallback)

<details>
<br />
<summary>Código inicial</summary>

```jsx
import { useState } from 'react'

const Timer = () => {
  const [seconds, setSeconds] = useState(150)

  return (
    <h1>
      <span>{seconds}</span>
    </h1>
  )
}

const App = () => {
  return (
    <>
      <h2>Um título qualquer</h2>
      <p>Um parágrafo qualquer</p>
      <Timer />
    </>
  )
}

export { App }
```

</details>

---

# 32. M2#A14 - Resolução da Bateria 14: Refactoring de Hook Personalizado, Edição de Nota de Filme, Evitar Request e Consertar o delay do timer

- [Regras dos Hooks](https://react.dev/warnings/invalid-hook-call-warning)

---

# 33. M2#A15 - Conceitos de SPA e Introdução ao React Router

- [Doc do React Router](https://reactrouter.com)

<details>
<br />
<summary>Comando para instlar o React Router de forma exata</summary>

```
npm i --save-exact react-router-dom@6.21.1
```

</details>

---

# 35. M2#A17 - Rotas e Layouts Aninhados no React Router

<details>
<br />
<summary>CSS usado na aula</summary>

```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

:root {
  --primary: #535353;
  --secondary: #ececec;
}

* {
  color: #535353;
  margin: 0;
}

body {
  margin: 0;
  padding: 20px;
  font-family: "Poppins";
  background: var(--secondary);
  text-align: center;
}

p {
  margin: 20px 0;
}

button {
  border: 0;
  padding: 12px 12px;
  border-radius: 4px;
  color: white;
  background: var(--primary);
  cursor: pointer;
}

header nav ul {
  display: flex;
  gap: 16px;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
  list-style: none;
}

header nav a {
  text-decoration: none;
  padding: 6px;
  border-radius: 4px;
}

header nav a.active {
  background: var(--primary);
  color: white;
}

main {
  max-width: 1200px;
  margin: 40px auto;
}


.help-layout nav {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin: 50px 0;
}

.help-layout nav a {
  padding: 10px;
  border: 2px solid var(--primary);
  border-radius: 4px;
  text-decoration: none;
}

.help-layout nav a:hover {
  border-color: var(--primary);
}

.help-layout nav a.active {
  background: var(--primary);
}

.faq .question {
  background: rgba(0, 0, 0, 0.1);
  padding: 5px 20px;
  border-radius: 4px;
  margin: 20px 0;
}

form {
  margin-top: 30px;
}

form input,
form label span,
form textarea {
  display: block;
}

form input,
form textarea {
  margin-bottom: 30px;
  padding: 8px;
  border-radius: 4px;
  border: 0;
  width: 300px;
  color: var(--primary);
}

form label {
  display: flex;
  flex-direction: column;
  align-items: center;
}

form label span {
  margin-bottom: 10px;
}

footer {
  margin-top: 70vh;
}
```

</details>
