## Integração backend e frontend

# Checklist

## Primeira requisição com Axios e useEffect

```
yarn add axios@0.27.2
```

## Listagem de vendas

Definição da BASE_URL:

```javascript
export const BASE_URL =
  import.meta.env.VITE_BACKEND_URL ?? "http://localhost:8080";
```

## Mensagem Toast de confirmação

```
yarn add react-toastify@9.0.5
```

No App.tsx:

```javascript
import { ToastContainer } from "react-toastify";
import "react-toastify/dist/ReactToastify.css";
```

## Deploy no Netlify

Acrescentar `window.React = React` no main.tsx:

```js
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App'
import './index.css'

window.React = React

ReactDOM.createRoot(document.getElementById('root') as HTMLElement).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
)
```

https://www.netlify.com/

- Deploy básico

  - Base directory: frontend
  - Build command: yarn build
  - Publish directory: frontend/dist
  - Variáveis de ambiente:
    - VITE_BACKEND_URL

- Configurações adicionais
  - Site settings -> Domain Management: (colocar o nome que você quiser)
  - Deploys -> Trigger deploy
