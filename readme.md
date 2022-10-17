# **Ignite Lab**

Construção de um Design System do Figma ao React.

## **Passo 1: Estrutura visual do Design System**
<br>

_Link do Figma:_ https://www.figma.com/file/HOvFtIz7hilJopiiU4uXp7/Ignite-Lab-Design-System?node-id=0%3A1

### O que é um Design System? 

    É uma convenção criada em empresas, principalmente quando se trabalha com múltiplos projetos e esses projetos seguem uma linha visual muito semelhante, onde são definidos conjuntos de padrões e práticas de criação compartilhadas de forma coerente, auxiliando a equipe de Design e Desenvolvimento a manter os padrões durante o desenvolvimento de produtos digitais como aplicativos ou sites.

### Atalhos Figma

- Setas - Move os objetos em 1px (Com o Shift selecionado move em 10px)
- A ou F - Seleciona a ferramenta de Frame para criar novas áreas de trabalho;
- T - Seleciona a ferramenta de Texto;
- R - Seleciona a ferramenta de Retangulo;
- K - Seleciona a ferramenta de Scale (Para manter o aspecto da borda conforme diminuir um objeto é a ferramente ideal);
- Alt (Com um objeto selecionado) - Quando o mouse sobrepõe outro objeto mostra a distância entre esses elementos (Dica: Utilizar as setas para diminuir ou aumentar essa distância);
- Ctrl + D - Duplica o objeto selecionado;
- Shift (Enquanto arrasta um objeto) - Mantém o elemento alinhado na horizontal ou vertical  com a sua posição inicial;
- Ctrl + G - Agrupa elementos selecionados;
- Dois Cliques ou Ctrl (Em objetos agrupados) - Seleciona um elemento dentro do grupo (essa seleção também pode ser feita através da janela de camadas (Layers);
- Ctrl + Alt + P - Inicia o último plugin utilizado;

### Ferramentas Figma

- **Auto Layout** - Funciona como o display flex na CSS, onde é possível ajustar os itens de acordo com o conteúdo ou tamanho do elemento pai. A ordem das camadas do elemento pai define a ordem dos elementos filhos;
- **Phosphor Icons** - Plugin de Ícones;
- **Selection colors** - Quando tem um conjunto de elementos selecionados o Figma apresenta uma lista com as cores que existem nessa seleção, sendo possível também alterar os nomes delas, para funcionar como variáveis do CSS para isso utilizamos o icone “Style” e clicamos em + para adicionar. Para criar uma sub classe, durante a criação utilizar /, por exemplo: ***grey/900***.


## **Passo 2: Do Figma ao React, criando aplicação**
<br>

### Criando e executando o projeto React

Primeiro configuramos o Vite usando o React, executamos o comando no Windows:

- npm create vite@latest

Digitamos o nome do projeto, escolhemos o framework e a linguagem. Depois acessamos o diretório do projeto e executamos o comando:

- npm i

Agora para executar o projeto, executamos o seguinte comando:

- npm run dev

### Configurando o Tailwind

- npm install -D tailwindcss postcss autoprefixer

- npx tailwindcss init -p

No arquivo tailwind.config.cjs inserir no vetor content o caminho do diretório a seguir:

- './src/**\/*.tsx'

### Importando fontes

Primeiro, importamos a fonte que desejamos usar do google fonts no index.html, depois no arquivo 
tailwind.config.cjs no objeto theme em extend a fontFamily default:

- fontFamily: { sans: 'Inter, sans-serif' },

### Setup do storybook

O storybook é uma ferramente que nos permite visualizar os componentes funcionando de forma isolada.

- npx sb init --builder @storybook/builder-vite --use-npm

- npm run storybook

### Importando tokens

Alteramos o arquivo tailwind.config.cjs, adicionando no objeto themes alguns tokens que criamos no figma, como as cores a serem utilizadas, o fontSize, etc.

### Criando componentes

-  npm install --save clsx

- npm install @radix-ui/react-slot

- npm i phosphor-react

npm install @radix-ui/react-checkbox