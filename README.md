# React \#02 e \#03

`npx create-react-app my-app --template typescript`

## Introdução ao React com TypeScript (#03)

- Chakra UI;
- Testes Automatizados:
  - Unitários: São testes que cobrem uma unidade de funcionamento da sua aplicação. O conceito de unidade é abstrato, mas tipicamente será um módulo com um propósito próprio, como uma função ou um componente em React.
  - de Integração: São testes que cobrem a integração entre diferentes partes da aplicação, ajudando a garantir que as diferentes partes da aplicação funcionem juntas corretamente.
  - e2e (ponta a ponta): São testes que cobrem todo o fluxo do usuário na aplicação, ajudando a garantir que a aplicação funcione corretamente do ponto de vista do usuário.
- Test Driven Development: O Test Driven Development (TDD) é uma abordagem de desenvolvimento de software que coloca um foco significativo na escrita de testes automatizados antes da implementação do código real. O processo do TDD segue um ciclo iterativo que envolve a criação dos testes, a implementação mínima necessária para fazer os testes passarem e, em seguida, a refatoração do código para melhorar sua qualidade.

## Conceitos Avançados de React com TypeScript (#04)

### Rotas

O React Router DOM permite criar aplicativos de página única (SPA) com navegação dinâmica, sem a necessidade de recarregar a página inteira.

`npm install react-router-dom`

```tsx
<BrowserRouter>
  <ChakraProvider>
    <Layout>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/conta/:id" element={<Conta />} />
        <Route path="/infoconta" element={<ContaInfo />} />
      </Routes>
    </Layout>
  </ChakraProvider>
</BrowserRouter>
```

### Estados Globais

A Context API é uma parte da biblioteca React que permite o compartilhamento eficiente de dados entre componentes em diferentes partes de uma aplicação, sem a necessidade de passar props manualmente de um componente para outro.

1: Criação do Contexto:

```tsx
import React, { createContext } from "react";

const MeuContexto = createContext();
```

2: Provedor do Contexto:

```tsx
<MeuContexto.Provider value={dadosCompartilhados}>
  {/* Seus componentes aqui */}
</MeuContexto.Provider>
```

3: Consumidor(es) do Contexto:

```tsx
import React, { useContext } from "react";

const dados = useContext(MeuContexto);
// Agora 'dados' contém os dados do contexto
```

### Local Storage

O Local Storage é uma API do navegador que permite que os aplicativos da web armazenem dados no navegador do usuário de forma persistente.

## Projetos

- [Criando uma Homepage com React](https://github.com/Err0rGCeni/DIOProject_ReactTSHome)
