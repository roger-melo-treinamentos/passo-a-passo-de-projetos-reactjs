## Passo a Passo de Projetos React JS

---

## 1. M1#A01 - Aula inaugural

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

## 3. M1#A03 - Resolução Bateria de Desafios 01 + Vite e Configuração do Ambiente

- [Como instalar o WSL no Windows](https://learn.microsoft.com/en-us/windows/wsl/install)
- [Developing in WSL](https://code.visualstudio.com/docs/remote/wsl)
- [Node JS](https://nodejs.org/en)
- [NVM](https://github.com/nvm-sh/nvm)
- [Vite](https://vitejs.dev/)
- [Semantic Versioning](https://semver.org/)
- [NPM Docs](https://docs.npmjs.com/cli/v10)
- [ESLint](https://eslint.org/)
- [Prettier](https://prettier.io/)

---

## 4. M1#A04 - ES Modules

- [Importing and Exporting Components - React docs](https://react.dev/learn/importing-and-exporting-components)

---

## 5. M1#A05 - StrictMode e O jeito certo de renderizar listas e manipular eventos

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

## 7. M1#A07 - Introdução a estado no React

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

## 8. M1#A08 - Introdução a estado no React - Parte 2

- [Queueing a Series of State Updates](https://react.dev/learn/queueing-a-series-of-state-updates)
- [Sharing State Between Components](https://react.dev/learn/sharing-state-between-components)

---

## 10. M1#A10 - Formulários controlados e não controlados

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

## 13. M1#A13 - Resetar form, estrutura de diretórios e próximo projeto

- [Queueing a Series of State Updates](https://react.dev/learn/queueing-a-series-of-state-updates)

---

## 16. M1#A16 - Lifecycle de um componente, Requests HTTP e hook useEffect

- [Keeping Components Pure](https://react.dev/learn/keeping-components-pure)
- [useEffect](https://react.dev/reference/react/useEffect)

---

## 20. M2#A02 - Atualização de dependências e Primeiras implementações da Bateria 09 (Me Avalia)

<details>
<br />
<summary>Comando para atualizar as dependências do vite-boilerplate</summary>

```
npm i --save-dev --save-exact @types/react@18.2.38 @types/react-dom@18.2.17 @vitejs/plugin-react@4.2.0 eslint@8.54.0 eslint-plugin-react@7.33.2 eslint-plugin-react-refresh@0.4.4 vite@5.0.2
```
</details>

---

## 22. M2#A04 - Hook useRef, hooks personalizados, imagens quebradas e reposicionamento de estado

- [Placeholder para imagens quebradas](assets/lessons/22/404-img.jpg)
- [useRef](https://react.dev/reference/react/useRef)
- [Ref x state](https://react.dev/learn/referencing-values-with-refs#differences-between-refs-and-state)

---

## 26. M2#A08 - Aliases no Vite e Hook useReducer

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

## 28. M2#A10 - Atualização de Dependências do vite-boilerplate e Apresentação do Próximo Projeto

<details>
<br />
<summary>Atualização de dependências com versões exatas</summary>

```
npm i --save-dev --save-exact @types/react@18.2.43 @vitejs/plugin-react@4.2.1 eslint@8.55.0 eslint-plugin-react-refresh@0.4.5 vite@5.0.7
```

</details>

---

## 31. M2#A13 - Delay em Timer, Dependências do useEffect, Memoização e Introdução ao Hook useCallback

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

## 32. M2#A14 - Resolução da Bateria 14: Refactoring de Hook Personalizado, Edição de Nota de Filme, Evitar Request e Consertar o delay do timer

- [Regras dos Hooks](https://react.dev/warnings/invalid-hook-call-warning)

---

## 33. M2#A15 - Conceitos de SPA e Introdução ao React Router

- [Doc do React Router](https://reactrouter.com)

<details>
<br />
<summary>Comando para instalar o React Router de forma exata</summary>

```
npm i --save-exact react-router-dom@6.21.1
```

</details>

---

## 35. M2#A17 - Rotas e Layouts Aninhados no React Router

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

---

## 38. M2#A20 - React Router: Loaders, Hooks useLoaderData e useParams, e Rotas Dinâmicas

<details>
<br />
<summary>CSS da lista de pessoas</summary>

```css
.people a {
  text-decoration: none;
}

.people li {
  list-style: none;
  text-align: left;
  background: rgba(0, 0, 0, 0.1);
  padding: 20px;
  border-radius: 4px;
  margin: 20px 0;
}

.people li:hover {
  background: rgba(0, 0, 0, 0.2);
}

.people h3 {
  font-size: 1.5rem;
}

.people p {
  margin: 0;
}
```

</details>

<details>
<br />
<summary>CSS do componente de detalhes da pessoa</summary>

```css
.person {
  list-style: none;
  text-align: left;
  background: rgba(0, 0, 0, 0.1);
  padding: 20px;
  border-radius: 4px;
  margin: 20px 0;
}

.person h2 {
  font-size: 2rem;
}

.person p {
  margin: 0;
}
```

</details>

---

## 41. M2#A23 - Integração de Mapa com a Biblioteca Leaflet e Hook useOutletContext do React Router

<details>
<br />
<summary>Atualização de dependências com versões exatas</summary>

```
npm i --save-exact @types/react@18.2.48 @types/react-dom@18.2.18 eslint@8.56.0 vite@5.0.12 react-router-dom@6.21.3
```

</details>

<details>
<br />
<summary>CSS inicial utilizado na aula</summary>

```css
.map-layout .container {
  display: flex;
  padding: 0;
  height: 40rem;
  margin: 2rem 0;
}

.map-layout .sidebar {
  display: flex;
  width: 50%;
  justify-content: center;
  align-items: center;
  background-color: white;
}

.map-layout .map {
  background-color: lightskyblue;
  flex-basis: 56rem;
}

.sidebar ul {
  list-style: none;
  padding: 0;
}

.sidebar li {
  border: #535353 1px solid;
  border-radius: .5rem;
  padding: 1rem 1.5rem;
  margin: 1.5rem;
  text-decoration: none;
}

.sidebar a {
  text-decoration: none;
}

.city-details {
  text-align: left;
  padding: 2rem 3rem;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.city-details p {
  margin: 0;
}
```

</details>

<details>
<br />
<summary>JSON utilizado na aula</summary>

```json
[
  {
    "id": 73930385,
    "name": "Buenos Aires",
    "country": "Argentina",
    "notes": "Enorme variedade de coisas para ver e fazer.",
    "position": {
      "latitude": -34.60449337161966,
      "longitude": -58.38935696465469
    }
  },
  {
    "id": 948723984,
    "name": "Curitiba",
    "country": "Brasil",
    "notes": "Cuidado com planejamento urbano, belas áreas verdes e transporte público de qualidade.",
    "position": {
      "latitude": -25.437370980404776,
      "longitude": -49.27058902123733
    }
  },
  {
    "id": 827477367346724,
    "name": "Budapeste",
    "country": "Hungria",
    "notes": "Uma das mais belas cidades da Europa. Arquitetura de deixar qualquer um de queixo caído.",
    "position": {
      "latitude": 47.49965441993388,
      "longitude": 19.038280069820203
    }
  },
  {
    "id": 750392432,
    "name": "Maringá",
    "country": "Brasil",
    "notes": "Qualidade de vida nota mil. Uma das cidades mais arborizadas e limpas do país.",
    "position": {
      "latitude": -23.42089821640173,
      "longitude": -51.9332036645167
    }
  },
  {
    "id": 674854,
    "name": "Ushuaia",
    "country": "Argentina",
    "notes": "Já ouviu falar do fim do mundo? Bonita, aconchegante e gelada.",
    "position": {
      "latitude": -54.80188821875919,
      "longitude": -68.30280605105817
    }
  }
]
```

</details>

<details>
<br />
<summary>Comando de instalação da leaflet e react-leaflet de forma exata</summary>

```
npm i --save-exact leaflet@1.9.4 react-leaflet@4.2.1
```

</details>

---

## 42. M2#A24 - Nova Rota Para Form de Adição de Cidades, Estado em URLs e Interação com o Mapa

<details>
<br />
<summary>CSS inicial utilizado na aula</summary>

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

.people a {
  text-decoration: none;
}

.people li {
  list-style: none;
  text-align: left;
  background: rgba(0, 0, 0, 0.1);
  padding: 20px;
  border-radius: 4px;
  margin: 20px 0;
}

.people li:hover {
  background: rgba(0, 0, 0, 0.2);
}

.people h3 {
  font-size: 1.5rem;
}

.people p {
  margin: 0;
}

.person {
  list-style: none;
  text-align: left;
  background: rgba(0, 0, 0, 0.1);
  padding: 20px;
  border-radius: 4px;
  margin: 20px 0;
}

.person h2 {
  font-size: 2rem;
}

.person p {
  margin: 0;
}

.person button {
  margin-top: 1rem;
}

.map-layout .container {
  display: flex;
  padding: 0;
  height: 40rem;
  margin: 2rem 0;
}

.map-layout .sidebar {
  display: flex;
  width: 50%;
  justify-content: center;
  align-items: center;
  background-color: var(--secondary);
}

.map-layout .map {
  flex-basis: 56rem;
  position: relative;
}

.map-container {
  height: 100%;
}

.sidebar ul {
  list-style: none;
  padding: 0;
}

.sidebar li {
  border: #535353 1px solid;
  border-radius: .5rem;
  padding: 1rem 1.5rem;
  margin: 1.5rem;
  text-decoration: none;
}

.sidebar a {
  text-decoration: none;
}

.city-details {
  text-align: left;
  padding: 2rem 3rem;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.city-details p {
  margin: 0;
}

.form-add-city {
  margin-top: 0;
  text-align: left;
}

.form-add-city input,
.form-add-city textarea {
  width: 95%;
}

.form-add-city label {
  align-items: normal;
}

.form-add-city .buttons {
  display: flex;
  justify-content: space-between;
}

.form-add-city .buttons button:first-child {
  border: 0;
  background-color: transparent;
  color: var(--primary);
}

.form-add-city .buttons button:last-child {
  background-color: #257eca;
}

.btn-geolocation {
  font-weight: 700;
  font-size: 1rem;
  position: absolute;
  z-index: 1000;
  bottom: 2rem;
  right: 1rem;
  background-color: var(--primary);
  color: var(--secondary);
  box-shadow: 0 0.4rem 1.2rem rgba(36, 42, 46, 0.16);
  padding-left: 1rem;
  padding-right: 1rem;
}
```

</details>

<details>
<br />
<summary>Marcação inicial do FormAddCity</summary>

```jsx
const FormAddCity = () =>
  <form className="form-add-city">
    <label>
      <span>Nome da cidade</span>
      <input />
    </label>
    <label>
      <span>Quando você foi para [NOME_DA_CIDADE]?</span>
      <input type="date" />
    </label>
    <label>
      <span>Suas anotações sobre a cidade</span>
      <textarea></textarea>
    </label>
    <div className="buttons">
      <button>&larr; Voltar</button>
      <button>Adicionar</button>
    </div>
  </form>
```

</details>

---

## 44. M2#A26 - Informações da Cidade Clicada no Mapa, Localização do Usuário, Objetos Request e URL

### Documentação das APIs Web mostradas na Aula

- [URL](https://developer.mozilla.org/en-US/docs/Web/API/URL)
- [Request](https://developer.mozilla.org/en-US/docs/Web/API/Request)

---

## 48. M3#A01 - Introdução a Context API

### Documentação da Context API

- [Before you use context](https://react.dev/learn/passing-data-deeply-with-context#before-you-use-context)
- [Passing Data Deeply with Context](https://react.dev/learn/passing-data-deeply-with-context)
- [createContext](https://react.dev/reference/react/createContext)
- [useContext](https://react.dev/reference/react/useContext)

### Código inicial utilizado na aula

<details>
<br />
<summary>CSS</summary>

```css
* {
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  margin: 20px;
  padding: 0;
}

ul {
  padding-inline-start: 20px;
  list-style-type: none; 
  padding: 0px 10px;
}

li { 
  margin-bottom: 10px; 
  display: grid; 
  grid-template-columns: auto 1fr;
  gap: 20px;
  align-items: center;
}

```

</details>

<details>
<br />
<summary>JSX</summary>

```jsx
import { useState } from 'react'

const games = [
  {
    id: '610aw15JvKL',
    name: `Assassin's Creed Mirage`,
    description: `Em Assassin's Creed Mirage, você é Basim, um astucioso ladino de rua em busca de respostas e de justiça.`,
    imgUrl: 'https://m.media-amazon.com/images/I/610aw15JvKL._AC_SL1000_.jpg',
  },
  {
    id: '61te8AW6zjL',
    name: 'EA Sports FC 24',
    description: 'O EA SPORTS FC 24 traz para você o Jogo de Todo Mundo.',
    imgUrl: 'https://m.media-amazon.com/images/I/61te8AW6zjL._AC_SL1020_.jpg',
  },
  {
    id: '81RfcW3Ml-L',
    name: `Marvel's Spider-Man 2`,
    description: `Peter Parker e Miles Morales retornam para uma nova e emocionante aventura na aclamada franquia de Marvel's Spider-Man.`,
    imgUrl: 'https://m.media-amazon.com/images/I/81RfcW3Ml-L._AC_SL1500_.jpg',
  }
]

const GamesList = ({ imgHeight }) =>
  <ul>
    {games.map(game =>
      <li key={game.id}>
        <Game game={game} imgHeight={imgHeight} />
      </li>
    )}
  </ul>

const Game = ({ game, imgHeight }) =>
  <>
    <Img game={game} imgHeight={imgHeight} />
    <p><b>{game.name}</b>{': ' + game.description}</p>
  </>

const Img = ({ game, imgHeight }) =>
  <img src={game.imgUrl} alt={game.name} style={{ height: imgHeight }} />

const App = () => {
  const [isLarge, setIsLarge] = useState(false)
  const imgHeight = isLarge ? 200 : 100
  const handleChange = e => setIsLarge(e.target.checked)
  return (
    <>
      <label>
        <input type="checkbox" checked={isLarge} onChange={handleChange} />
        Ver imagens maiores
      </label>
      <hr />
      <GamesList imgHeight={imgHeight} />
    </>
  )
}

export { App }
```

</details>

---

## 53. M3#A06 - Rotas Públicas e Privadas com React Router

<details>
<br />
<summary>Objeto usado na aula</summary>

```js
const fakeAuthProvider = {
  isAuthenticated: false,
  email: null,
  signIn: async function (email) {
    await new Promise(resolve => setTimeout(resolve, 500))
    this.isAuthenticated = true
    this.email = email
  },
  signOut: async function () {
    await new Promise(resolve => setTimeout(resolve, 500))
    this.isAuthenticated = false
    this.email = null
  }
}
```

</details>

---

## 56. M3#A09 - Próxima Versão do React e Memoização com Memo

<details>
<br />
<summary>Código inicial usado na aula</summary>

```css
body {
  background-color: #232323;
  color: white;
}

```

```jsx
import { useState } from 'react'

const List = ({ items }) =>
  <ul>
    {items.map(item => <li key={item}>{item}</li>)}
  </ul>

const Title = ({ text }) => <h1>{text}</h1>

const App = () => {
  const [items, setItems] = useState([])
  const handleClick = () => setItems(prev => [...prev, `Item ${prev.length + 1}`])
  return (
    <>
      <Title text="Olá" />
      <button onClick={handleClick}>Criar item</button>
      <List items={items} />
    </>
  )
}

export { App }

```

</details>

---

## 57. M3#A10 - O Hook useMemo e Regras do ESLint

<details>
<br />
<summary>Código inicial para o segundo exemplo com o Hook useMemo</summary>

```css
body {
  background-color: #232323;
  color: white;
}

h2 {
  margin-bottom: .5rem;
}

.counters {
  display: flex;
  flex-direction: column;
  gap: 3rem;
}
```

```jsx
import { useState } from 'react'

const App = () => {
  const [counter, setCounter] = useState(0)
  const [anotherCounter, setAnotherCounter] = useState(0)
  const incrementCounter = () => setCounter(prev => prev + 1)
  const incrementAnotherCounter = () => setAnotherCounter(prev => prev + 1)
  const result = Array.from({ length: counter + 10_000_000 }).length
  return (
    <div className="counters">
      <div>
        <h2>Contador: {counter}</h2>
        <button onClick={incrementCounter}>Incrementar</button>
      </div>
      <div>
        <h2>Outro contador: {anotherCounter}</h2>
        <button onClick={incrementAnotherCounter}>Incrementar</button>
      </div>
      <h1>Resultado: {result}</h1>
    </div>
  )
}

export { App }
```

</details>

<details>
<br />
<summary>Código inicial para o terceiro exemplo com o Hook useMemo (🟡 não execute antes de ver a aula)</summary>

```css
body {
  background-color: #232323;
  color: white;
}
```

```jsx
import { useState, useEffect } from 'react'

const useFetch = options => {
  const [data, setData] = useState([])

  useEffect(() => {
    if (options.url) {
      fetch(options.url)
        .then(r => r.json())
        .then(data => setData(data))
        .catch(error => console.log(error.message))
    }
  }, [options])

  return { data }
}

const App = () => {
  const [url, setUrl] = useState('')
  const { data } = useFetch({ url })
  const setUsersUrl = () => setUrl('https://jsonplaceholder.typicode.com/users')
  const setCitiesUrl = () => setUrl('') // 👈🏻 sua API fake aqui
  return (
    <div className="app">
      <button onClick={setUsersUrl}>Show users</button>
      <button onClick={setCitiesUrl}>Show cities</button>
      <ul>
        {data.map(item => <li key={item.id}>{item.name}</li>)}
      </ul>
    </div>
  )
}

export { App }
```

</details>

---

## 59. M3#A12 - Quando Usar o Hook useCallback e Introdução a Otimização do Tamanho do Bundle com Code Splitting

<details>
<br />
<summary>Código inicial para o 1º exemplo (contém erro de lint proposital)</summary>

```css
body {
  background-color: #2f2f3d;
  color: white;
}

```

```jsx
import { useEffect, useState } from 'react'

const useCounter = () => {
  const [count, setCount] = useState(0)
  const increment = () => setCount(prev => prev + 1)
  return { count, increment }
}

const App = () => {
  const { count, increment } = useCounter()

  useEffect(() => {
    increment()
  }, [])

  return (
    <>
      <h2>{count}</h2>
      <p>Um parágrafo qualquer</p>
      <button onClick={increment}>Incrementar</button>
    </>
  )
}

export { App }

```

</details>

<details>
<br />
<summary>Código inicial para o 2º exemplo (contém lentidão de componente proposital)</summary>

```css
label span {
  display: block;
  margin-top: 1rem;
}

.btn-send {
  display: block;
  margin-top: .5rem;
}

.padding {
  padding: 1rem;
}

.light {
  background-color: white;
  color: #3a3a3a;
}

.dark {
  background-color: #3a3a3a;
  color: white;
}

.count {
  display: inline-block;
  margin: .5rem .5rem 1rem;
}
```

```jsx
import { useState, memo } from 'react'

const Form = memo(({ onSubmit }) => {
  const [count, setCount] = useState(1)

  const startTime = performance.now()
  while (performance.now() - startTime < 500) {
    // Faz nada durante 500 milisegundos, para emular um delay
  }

  const handleSubmit = e => {
    e.preventDefault()
    const formData = Object.fromEntries(new FormData(e.target))
    onSubmit({ count, ...formData })
  }

  const increment = () => setCount(count + 1)
  const decrement = () => setCount(count - 1)

  return (
    <form onSubmit={handleSubmit}>
      <label>
        <span>Quantidade:</span>
        <button type="button" onClick={decrement}>-</button>
        <span className="count">{count}</span>
        <button type="button" onClick={increment}>+</button>
      </label>
      <label>
        <span>Rua:</span>
        <input name="street" />
      </label>
      <label>
        <span>Cidade:</span>
        <input name="city" />
      </label>
      <label>
        <span>CEP:</span>
        <input name="zipCode" />
      </label>
      <button type="submit" className="btn-send">Enviar</button>
    </form>
  )
})

const ProductPage = ({ productId, referrerId, theme }) => {
  const handleSubmit = orderDetails => post(`/product/${productId}/buy`, { referrerId, orderDetails })
  return (
    <div className={`${theme} padding`}>
      <Form onSubmit={handleSubmit} />
    </div>
  )
}

const post = (url, data) => console.log({ url: `POST ${url}`, data })

const App = () => {
  const [isDark, setIsDark] = useState(false)
  const toggleDarkMode = e => setIsDark(e.target.checked)
  return (
    <>
      <label>
        <input type="checkbox" checked={isDark} onChange={toggleDarkMode} />
        Tema escuro
      </label>
      <hr />
      <ProductPage referrerId="wizard_of_oz" productId={123} theme={isDark ? 'dark' : 'light'} />
    </>
  )
}

export { App }
```

</details>

---

## 60. M3#A13 - Otimização do Tamanho do Bundle com Code Splitting - Parte 2

- [Repositório inicial para esta aula](https://github.com/Roger-Melo/react-code-splitting)

---

## 62. M3#A15 - Introdução a React Query (TanStack Query): O Que É, Por que Usar e Correlação com React Router

- [Doc do React Query](https://tanstack.com/query/latest/docs/framework/react/overview)

<details>
<br />
<summary>Código inicial para o 1º exemplo</summary>

```jsx
import { useEffect, useState } from 'react'

const url = 'https://www.random.org/integers/?num=1&min=1&max=100&col=5&base=10&format=plain&rnd=new'

const RandomNumber = () => {
  const [randomNumber, setRandomNumber] = useState(null)

  useEffect(() => {
    fetch(url)
      .then(response => response.json())
      .then(number => setRandomNumber(number))
      .catch(error => alert(`Error message: ${error.message}`))
  }, [])

  return <h2>Número aleatório: {randomNumber}</h2>
}

const App = () => <RandomNumber />

export { App }

```

</details>

<details>
<br />
<summary>Comando para instalar React Query e o Plugin do ESLint, de forma exata</summary>

```
npm i --save-exact @tanstack/react-query@5.28.4 @tanstack/eslint-plugin-query@5.27.7
```

</details>

<details>
<br />
<summary>Inserção do plugin nas extensões do .eslintrc.cjs</summary>

```
"plugin:@tanstack/eslint-plugin-query/recommended"
```

</details>

---

## 64. M3#A17 - Requests com React Query

- [Doc da API do GitHub](https://docs.github.com/en/rest)

<details>
<br />
<summary>Endpoint do primeiro request</summary>

```javascript
`https://api.github.com/users/${username}`
```

</details>

<details>
<br />
<summary>Exemplo para o 2º request</summary>

```css
ul {
  list-style: none;
}

.issuesList {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.issuesList li {
  border: .1rem solid lightgrey;
  padding: 1rem;
  border-radius: 1rem;
  max-width: 50%;
}

.createdBy {
  display: flex;
  gap: .5rem;
  align-items: center;
}

.createdBy img {
  width: 2rem;
  height: 2rem;
  border-radius: 50%;
}

.labels span {
  display: inline-block;
  padding: .3rem 0.7rem;
  border-radius: 0.4rem;
  margin-right: .3rem;
}

```

```javascript
const fetchIssues = ({ organization, repository }) =>
  fetch(`https://api.github.com/repos/${organization}/${repository}/issues`)
    .then(res => res.json())
    .then(data => {
      return data.map(issue => ({
        id: issue.id,
        state: issue.state,
        title: issue.title,
        createdAt: issue.created_at,
        author: { name: issue.user.login, avatar: issue.user.avatar_url },
        labels: issue.labels.map(label => ({ id: label.id, color: label.color, name: label.name })),
        url: issue.html_url
      }))
    })

const getFormattedDate = date => {
  const [year, month, day] = date.split('T')[0].split('-')
  return `${day}/${month}/${year}`
}

const IssueItem = ({ state, title, createdAt, labels, author, url }) =>
  <li>
    <span>{state}</span>
    <h3>
      <a href={url} target="_blank" rel="noreferrer">{title}</a>
    </h3>
    <div className="createdBy">
      <p>Criada em {getFormattedDate(createdAt)}, por {author.name}</p>
      <img src={author.avatar} alt={`Foto de ${author.name}`} />
    </div>
    {labels.length > 0 && (
      <p className="labels">Labels: {labels.map(({ id, color, name }) =>
        <span key={id} style={{ backgroundColor: `#${color}` }}>{name}</span>)}
      </p>
    )}
  </li>

const IssuesList = () => {
  // 🦜 sua implementação aqui. 
  // Dica: você pode passar 'frontendbr' como organization e 'vagas' como repository

  return isError
    ? <p>{error.message}</p>
    : isLoading
      ? <p>Carregando informações...</p>
      : (
        <>
          <h1>Vagas</h1>
          <ul className="issuesList">{data.map(issue => <IssueItem key={issue.id} {...issue} />)}</ul>
        </>
      )
}

const App = () => <IssuesList />

export { App }

```

</details>

---

## 66. M3#A19 - Filtrando Vagas do Front-End BR Através das Labels

<details>
<br />
<summary>CSS inicial</summary>

```css
ul {
  list-style: none;
  padding-inline-start: 0;
}

.app {
  display: flex;
  gap: 1rem;
  max-width: 80rem;
  margin: auto;
  padding-top: 2rem;
}

.issuesListContainer {
  width: 50rem;
}

.issuesList {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.issuesList li {
  border: .1rem solid lightgrey;
  padding: 1rem;
  border-radius: 1rem;
}

.createdBy {
  display: flex;
  gap: .5rem;
  align-items: center;
}

.createdBy img {
  width: 2rem;
  height: 2rem;
  border-radius: 50%;
}

.label {
  padding: .3rem 0.7rem;
  border-radius: 0.4rem;
  margin-right: .3rem;
  border-width: 0;
}

.label:hover {
  cursor: pointer;
}

.labelsListContainer {
  width: 28rem;
}

.labelsList .label {
  margin-bottom: .4rem;
}

.labelsList {
  display: flex;
  flex-wrap: wrap;
}

.activeLabel {
  filter: opacity(.3);
}

```

</details>

---

## 71. M3#A24 - Eliminação de Repetição em Queries, Redundância em Argumentos e Bug Fix ao Filtrar Vagas por Labels

- [QueryClient](https://tanstack.com/query/latest/docs/reference/QueryClient)
- [Query Function Variables](https://tanstack.com/query/latest/docs/framework/react/guides/query-functions#query-function-variables)
- [Search by label](https://docs.github.com/en/search-github/searching-on-github/searching-issues-and-pull-requests#search-by-label)
- [URL API](https://developer.mozilla.org/en-US/docs/Web/API/URL_API)

---

## 74. M3#A27 - Error Boundaries

- [Catching rendering errors with an error boundary](https://react.dev/reference/react/Component#catching-rendering-errors-with-an-error-boundary)
- [react-error-boundary](https://github.com/bvaughn/react-error-boundary)
- [Sentry Reviews](https://www.g2.com/products/sentry/reviews)

<details>
<br />
<summary>JSX inicial</summary>

```jsx
import { useState } from 'react'

const Movies = ({ movies }) =>
  <ul>
    {movies.map(movie => <li key={movie.imdbID}>{movie.Title}</li>)}
  </ul>

const App = () => {
  const [movies, setMovies] = useState([])

  const fetchMovies = () => {
    fetch(/* seu endpoint aqui */)
      .then(res => res.json())
      .then(data => setMovies(data))
  }

  return (
    <>
      <button onClick={fetchMovies}>Buscar filmes</button>
      <Movies movies={movies} />
    </>
  )
}

export { App }
```

</details>

---

## Bônus: Aprenda Next.js

## 1. O que é o Next.js, por que usá-lo, instalação e configurações iniciais, App Router x Pages Router

- [Next.js Docs](https://nextjs.org/docs)

### Versões exatas usadas na aula

| Dependency / DevDependency | Version |
| :---: | :---: |
| create-next-app | 14.2.2 |
| react | 18.2.0 |
| react-dom | 18.2.0 |
| eslint | 8.57.0 |

---

## 4. Fundamentos de renderização, 6 passos do request-response lifecycle e prerendering

- [Rendering](https://nextjs.org/docs/app/building-your-application/rendering)
- [How Google Search indexes JavaScript sites - JavaScript SEO](https://youtu.be/LXF8bM4g-J4?si=PcFtVJysvdUv_wC3)

---

## 5. Resolução Bateria 31: React server components, client components, dev x production server e links de navegação

- [Introducing Zero-Bundle-Size React Server Components](https://react.dev/blog/2020/12/21/data-fetching-with-react-server-components)
- [When to use Server and Client Components](https://nextjs.org/docs/app/building-your-application/rendering/composition-patterns)
- [Linking and Navigating](https://nextjs.org/docs/app/building-your-application/routing/linking-and-navigating)

---

## 6. Client-side navigation, tamanho de um React Server Component, visualizando partial rendering e estilização no Next

- [Imagens desafio 2](assets/lessons/bonus-next-js/06)

### Versões exatas usadas na aula

| Dependency / DevDependency | Version |
| :---: | :---: |
| tailwindcss | 3.4.3 |
| postcss | 8.4.38 |
| autoprefixer | 10.4.19 |

<details>
<br />
<summary>RootLayout estilizado</summary>

```jsx
import Link from 'next/link'
import './globals.css'

const RootLayout = ({ children }) => {
  return (
    <html lang="pt-BR">
      <body className="bg-slate-800 text-slate-200 flex flex-col px-6 py-2 min-h-screen">
        <header>
          <nav className="flex justify-between border-b border-b-slate-600 pb-4 pt-2">
            <h2>Análises de Jogos</h2>
            <ul className="flex gap-4">
              <li>
                <Link href="/" className="hover:text-sky-500">Início</Link>
              </li>
              <li>
                <Link href="/sobre" prefetch={false} className="hover:text-sky-500">Sobre</Link>
              </li>
              <li>
                <Link href="/analises" className="hover:text-sky-500">Análises</Link>
              </li>
            </ul>
          </nav>
        </header>
        <main className="grow py-3">
          {children}
        </main>
        <footer className="border-t border-t-slate-600 py-3 text-center text-xs">
          Informações e imagens dos jogos gentilmente cedidos por{' '}
          <a href="https://rawg.io/" target="_blank" className="hover:text-sky-500">RAWG</a>
        </footer>
      </body>
    </html>
  )
}

export default RootLayout
```

</details>

---

## 7. Static assets, Layout shift e Otimização de imagens com o componente Image

### Imagens

- [Imagens dos Jogos](assets/lessons/bonus-next-js/07/game-images)
- [Screenshot do Desafio](assets/lessons/bonus-next-js/07/challenge-screenshot-images)

### Referências

- [alt attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#attributes)
- [Static Assets](https://nextjs.org/docs/app/building-your-application/optimizing/static-assets)
- [Image Optimization](https://nextjs.org/docs/app/building-your-application/optimizing/images)
- [Largest Contentful Paint (LCP)](https://web.dev/articles/lcp)
- [Images without dimensions](https://web.dev/articles/optimize-cls#images-without-dimensions)
- [Intrinsic size](https://developer.mozilla.org/en-US/docs/Glossary/Intrinsic_Size)
- [WebP - An image format for the Web](https://developers.google.com/speed/webp)
- [srcset attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#srcset)

---

## 9. Leitura de arquivos e Renderização de markdown

<details>
<br />
<summary>Marcação da Homepage</summary>

```jsx
const Home = () => {
  return (
    <>
      <div className="rounded-lg border-2 border-slate-700 w-1/2 hover:shadow-lg">
        <Link href="/analises/sonic-frontiers" className="flex">
          <Image
            src="/images/sonic-frontiers.jpg"
            width="320"
            height="180"
            alt=""
            priority
            className="rounded-l-lg"
          />
          <div className="p-3">
            <h2 className="text-xl font-montserrat">Sonic Frontiers - Análise</h2>
            <p>Breve parágrafo aqui</p>
          </div>
        </Link>
      </div>
    </>
  )
}
```

</details>

### Referências

- [Screenshot do Desafio Markdown Renderizado](assets/lessons/bonus-next-js/09/analise-sonic-frontiers.jpg)
- [The Markdown Guide](https://www.markdownguide.org/)
- [No async client component](https://nextjs.org/docs/messages/no-async-client-component)
- [React Server Component RFC on promise support](https://github.com/acdlite/rfcs/blob/first-class-promises/text/0000-first-class-support-for-promises.md)
- [Async components with Server Components](https://react.dev/reference/rsc/server-components#async-components-with-server-components)
- [How to Load Data from a File in Next.js](https://vercel.com/guides/loading-static-file-nextjs-api-route)
- [Runtimes](https://nextjs.org/docs/app/building-your-application/rendering/edge-and-nodejs-runtimes)
- [Reading files with Node.js](https://nodejs.org/en/learn/manipulating-files/reading-files-with-nodejs)
- [fsPromises.readFile(path[, options])](https://nodejs.org/docs/latest/api/fs.html#fspromisesreadfilepath-options)
  - 👆🏻 atenção: ao abrir o link acima, pode acontecer uma rolagem para um outro lugar da página. Neste caso, use `Ctrl + F` e pesquise pelo texto do link (neste caso, `fsPromises.readFile(path[, options])`).
- [isomorphic-dompurify](https://github.com/kkomelin/isomorphic-dompurify)
- [jsdom](https://github.com/jsdom/jsdom)

---

## 10. Resolução Bateria 33: Dynamic Routes, Slugs, Frontmatter, gray-matter e @tailwindcss/typography

- [tailwindcss-typography](https://github.com/tailwindlabs/tailwindcss-typography)
- [gray-matter](https://github.com/jonschlinkert/gray-matter)
- [`<time>`: The (Date) Time element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time)
- [Dynamic Routes](https://nextjs.org/docs/app/building-your-application/routing/dynamic-routes)

---

## 11. 🚧 Título em andamento

<details>
<br />
<summary>Conteúdo para a análise de Bloodborne</summary>

```md
__Bloodborne__ (ブラッドボーン Buraddobōn?) é um RPG eletrônico de ação produzido pela FromSoftware e publicado pela Sony Computer Entertainment a 24 de Março de 2015 em exclusivo para a PlayStation 4, sendo o quarto game da serie Souls.

Bloodborne foi realizado por Hidetaka Miyazaki, diretor de Demon's Souls e Dark Souls. Miyazaki afirmou que o jogo nunca foi produzido com o sentido de ser Demon's Souls II, porque a Sony Computer Entertainment queria uma nova IP para a PlayStation 4. 

Foi anunciado pela Sony a 9 de junho de 2014 durante a Electronic Entertainment Expo 2014, onde foi bem recebido pela critica ganhando diversos prêmios e nomeações. Bloodborne foi descrito por Paul Sullivan da Sony como "Dark Souls com Caçadeiras".
```

</details>

### Referências

- [fsPromises.readdir(path[, options])](https://nodejs.org/docs/latest/api/fs.html#fspromisesreaddirpath-options)
  - 👆🏻 atenção: ao abrir o link acima, pode acontecer uma rolagem para um outro lugar da página. Neste caso, use `Ctrl + F` e pesquise pelo texto do link (neste caso, `fsPromises.readdir(path[, options])`).

---

## 12. Resolução Bateria 34: Atualização Next.js, SSG, SSR, generateStaticParams e páginas estáticas para segmento dinâmico

- [Server Rendering Strategies](https://nextjs.org/docs/app/building-your-application/rendering/server-components#server-rendering-strategies)
- [Server Components](https://nextjs.org/docs/app/building-your-application/rendering/server-components)
- [Generating Static Params](https://nextjs.org/docs/app/building-your-application/routing/dynamic-routes#generating-static-params)

---

## 13. Resolução Bateria 34 - Pt 02 (Refactoring obtenção de slugs, Ordenação de análises) e Metadata em segmentos estáticos e dinâmicos

- [Favicon](assets/lessons/bonus-next-js/13/icon.png)

### Referências

- [Metadata](https://nextjs.org/docs/app/building-your-application/optimizing/metadata)
- [Basic Fields](https://nextjs.org/docs/app/api-reference/functions/generate-metadata#basic-fields)
- [Metadata Files API Reference](https://nextjs.org/docs/app/api-reference/file-conventions/metadata)

---

## 14. Client components aninhados, hydration, escrita no clipboard e lib de ícones

<details>
<br />
<summary>JSX time e button</summary>

```jsx
<div className="flex gap-4 items-baseline">
  <time dateTime={date}>{`${day}/${month}/${year}`}</time>
  <button className="border px-3 py-1 rounded text-slate-200 text-sm">Compartilhar</button>
</div>
```

</details>

### Referências

- ["What is hydration?"](https://nextjs.org/docs/app/building-your-application/rendering/client-components#full-page-load)
- [Prerendering & Hydration tweet](https://x.com/leeerob/status/1506287021823823876)
- [Clipboard: writeText() method](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard/writeText)
- [Location: href property](https://developer.mozilla.org/en-US/docs/Web/API/Location/href)
- [Slide da árvore de componentes](assets/lessons/bonus-next-js/14/tree-slide.jpg)
- [Terminology](https://nextjs.org/docs/app/building-your-application/routing#terminology)
- [Heroicons](https://heroicons.com/)
- [Lucide](https://lucide.dev/)

---

## 15. Resolução bateria 35 (Deploy na Vercel), Segunda fase do projeto game-reviews, JAMStack e Introdução a Headless CMS

- [Static Exports](https://nextjs.org/docs/app/building-your-application/deploying/static-exports)
- [Deploying](https://nextjs.org/docs/app/building-your-application/deploying)
- [Self-Hosting (servidor próprio)](https://nextjs.org/docs/app/building-your-application/deploying#self-hosting)
  - [Static Export: How To Install Nginx on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-22-04)
  - [Full-stack features: How To Set Up a Node.js Application for Production on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-node-js-application-for-production-on-ubuntu-20-04)
- [Working with domains](https://vercel.com/docs/projects/domains/working-with-domains)
- [Registro BR](https://registro.br/ajuda/)
- [Headless CMS](https://jamstack.org/headless-cms/)

---

## 16. Apresentação do CMS (Strapi) e projeto pré-configurado

- [Projeto pré-configurado](assets/lessons/bonus-next-js/16/cms-game-reviews.zip)

---

## 18. Resolução Bateria 36 (migração de Markdown para CMS): atualização das funções getReviews, getReview e getReviewSlugs

- [remotePatterns](https://nextjs.org/docs/app/api-reference/components/image#remotepatterns)

---

## 19. Mais detalhes sobre o componente Image: Next server como proxy, cache, priority e lazy loading de imagens

- [Image Optimization Diagram](assets/lessons/bonus-next-js/19/image-optimization-diagram.jpg)
- [Homepage Screenshot](assets/lessons/bonus-next-js/19/homepage-desafio-aula-19.jpg)

---

## 20. Renderização dinâmica de análises, cache de fetch requests, revalidate, dynamic e dynamicParams

- [logging](https://nextjs.org/docs/app/api-reference/next-config-js/logging)
- [dynamicParams](https://nextjs.org/docs/app/api-reference/file-conventions/route-segment-config#dynamicparams)
- [Features that require a Node.js server](https://nextjs.org/docs/app/building-your-application/deploying/static-exports#unsupported-features)
- [Caching Data](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating#caching-data)
- [dynamic](https://nextjs.org/docs/app/api-reference/file-conventions/route-segment-config#dynamic)
- [Opting out of Data Caching](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating#opting-out-of-data-caching)

---

## 22. Time-based revalidation, revalidação a nível de fetch e de página

<details>
<br />
<summary>generateStaticParams</summary>

```js
const generateStaticParams = async () => {
  const slugs = await getReviewSlugs()
  return slugs.map(slug => ({ slug }))
}
```

</details>

<details>
<br />
<summary>getReviewSlugs</summary>

```js
import { stringify } from 'qs'

const query = '?' + stringify({
  fields: ['slug'],
  sort: ['publishedAt:desc'],
  pagination: { pageSize: 100 }
}, { encodeValuesOnly: true })

const cmsBaseUrl = 'http://localhost:1337'

const getReviewSlugs = async () => fetch(`${cmsBaseUrl}/api/reviews${query}`)
  .then(res => res.json())
  .then(({ data }) => data.map(({ attributes }) => attributes.slug))
  .catch(console.log)

export { getReviewSlugs }
```

</details>

### Referências

- [Data Fetching, Caching, and Revalidating](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating)
- [Caching in Next.js](https://nextjs.org/docs/app/building-your-application/caching)

---

## 23. Route handlers, Webhooks, On-demand revalidation e revalidateTag

- [On-demand Revalidation](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating#on-demand-revalidation)
- [revalidateTag](https://nextjs.org/docs/app/api-reference/functions/revalidateTag)
- [Route Handlers](https://nextjs.org/docs/app/building-your-application/routing/route-handlers)
- [route.js](https://nextjs.org/docs/app/api-reference/file-conventions/route)
- [NextResponse](https://nextjs.org/docs/app/api-reference/functions/next-response)
- [Response](https://developer.mozilla.org/en-US/docs/Web/API/Response)
- [NextRequest](https://nextjs.org/docs/app/api-reference/functions/next-request)
- [Request](https://developer.mozilla.org/en-US/docs/Web/API/Request)
- [204 No Content](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/204)

---

## 25. Comparação de estratégias de renderização

- [Slides](assets/lessons/bonus-next-js/25/slides/)
- [Screenshot - exibição total de páginas](assets/lessons/bonus-next-js/25/exibicao-total-paginas.png)
