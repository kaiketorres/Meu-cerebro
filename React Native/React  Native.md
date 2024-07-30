## Introdução ao React Native

### O que é React Native?

React Native é uma biblioteca de código aberto criada pelo Facebook para desenvolver aplicativos móveis usando [[Javascript]] e React. Com ele, é possível criar aplicativos para iOS e Android a partir de um único código-base.

### Por que usar React Native?

- **Desenvolvimento Rápido**: O React Native permite a reutilização de código entre plataformas, o que acelera o desenvolvimento.
- **Comunidade Ativa**: Há uma grande comunidade de desenvolvedores que contribuem com bibliotecas e ferramentas.
- **Desempenho**: Os aplicativos criados com React Native têm desempenho próximo ao dos aplicativos nativos.
- **Hot Reloading**: Essa funcionalidade permite ver as mudanças no código imediatamente sem recompilar a aplicação.

### Conceitos Básicos

1. **Componentes**: São os blocos de construção dos aplicativos React Native. Você pode pensar neles como "widgets" ou "elementos de interface".
2. **JSX**: Assim como no React para web, o React Native usa JSX, uma sintaxe que permite escrever HTML dentro do JavaScript.
3. **Estilização**: No React Native, você estiliza componentes usando um objeto de estilo que se assemelha ao CSS, mas com algumas diferenças.

### Configuração do Ambiente

Para começar com o React Native, você precisará configurar seu ambiente de desenvolvimento. Aqui está um guia rápido:

1. **Node.js**: Instale o Node.js, que inclui o npm (Node Package Manager).

2. **Expo CLI**: Expo é uma ferramenta que facilita o desenvolvimento com React Native.

```
npm install -g expo-cli
```

3. **Criar um Projeto**:

```
expo init MeuPrimeiroApp
cd MeuPrimeiroApp
expo start
```
### Estrutura de um Projeto React Native

Após criar um projeto com Expo, você verá uma estrutura semelhante a esta:

```
MeuPrimeiroApp
├── App.js
├── app.json
├── node_modules
├── package.json
└── assets
```

- **App.js**: O ponto de entrada do seu aplicativo.
- **app.json**: Configurações do aplicativo.
- **assets**: Imagens e outros recursos estáticos.

### Criando Seu Primeiro Componente

Aqui está um exemplo simples de um componente React Native:

```
import React from 'react';
import { Text, View, StyleSheet } from 'react-native';

export default function App() {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>Olá, React Native!</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#f5fcff',
  },
  text: {
    fontSize: 20,
    textAlign: 'center',
    margin: 10,
  },
});
```

### Princípios de Estilização

Em React Native, você usa o objeto `StyleSheet` para criar estilos:

- **Flexbox**: Usado para layout, semelhante ao CSS Flexbox.
- **Propriedades de Estilo**: São camelCase, por exemplo, `backgroundColor` em vez de `background-color`.

### Navegação

Para adicionar navegação entre telas, você pode usar bibliotecas como React Navigation:

```
npm install @react-navigation/native @react-navigation/stack
```

### Recursos Úteis

- **Documentação Oficial**: React Native
- **Expo**: Expo Documentation
- **Tutoriais e Cursos**: Existem muitos tutoriais gratuitos e pagos que podem ajudar a aprofundar seus conhecimentos.
