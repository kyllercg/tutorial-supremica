# Tutorial Supremica
Minitutorial sobre como usar o Supremica.

## O que é o Supremica?

## Instalação

> Windows
>

> Linux
> 

## Conceitos introdutórios

1. Eventos:\
    Parte essencial, representam ações que provocam uma mudança no sistema. Esses eventos, também chamados de __transições__, são capazes de ligar estados e possuem um momento específico de ocorrência que desencadeia a transição de um estado para outro. 
2. Estados:\
    Em sistemas a eventos discretos os estados representam a condições, ou ainda status, do sistema em determinado momento, momento esse definido após determinada transição. A transição de um estado para outro é desencadeada por eventos específicos. São eles que determinam a saída e ditam o ponto inicial do sistema.
    
    O estados também podem ser classificados em 4 tipos:
       - Inicial
       - Marcado
       - Não marcado
       - Proibido
3. Linguagens:\
    Quando há uma sequência de estados, relacionados com eventos, o comportamento de um sistema a eventos discretos pode ser descrito por essa sequência, tal desempenho é modelado por uma linguagem.
    
    Todo SED está associado à um conjunto de eventos $E$, esse conjunto é pensado como o alfabeto e sequências desses eventos são pensadas como palavras dessa linguagem, ou ainda strings. 

4. Autômatos Finitos:\
    Método capaz de representar linguagens e lógicas, na forma de grafos, através de eventos e estados.

<p align="center">
  <img src="./imagens/automato.png" alt="Exemplo de um autômato"/>
</p>


      Sobre a figura acima, os nós são os estados, enquanto que as setas representam os eventos. Em essência, um autômato é uma abstração matemática que descreve um sistema que passa de um estado para outro em resposta a um conjunto de regras.

5. Autômato Finito Extendido:\
    Um outro tipo de autômato que utiliza do conceito de __guardas__ e __ações__ para ler e atualizar variáveis enquanto executa transições. Guardas são utilizados para permitir um evento sobre certas condições, já uma ação é o ato de mudar o estado de determinada variável.
    
    O estado de algo pode ser uma variável e seus valores são mudadas pelas ações e monitoradas pelos guardas. Eventos podem ser controlados por certos estados das variáveis a partir dos guardas.

6. Planta:\
   É o modelo do sistema que você deseja controlar. Ele representa o comportamento do sistema real que você deseja controlar. O modelo Plant é usado para gerar um controlador que pode ser implementado no sistema real.
   
7. Especificação:\
   É uma descrição formal das propriedades que o controlador deve satisfazer. O modelo Specification é usado para verificar se o controlador gerado a partir do modelo Plant satisfaz as propriedades especificadas.

## Criando um Autômato Finito

1. **Crie um módulo:**
   - Abra o Supremica e clique em `File > New `

2. **Crie uma Automato**.
   - Clique em `Create > New Automaton`
   - Digite o nome do automato 
   - Escolha o tipo (Kind) do automato como Planta (Plant).
   - Clique em `OK`

3. **Adicione estados e transições:**
   - Para adicionar um estado, clique no botao `circulo preto` do menu superior e clique nos pontos da malha quadriculada onde você deseja colocar os estados.
   - Para adicionar uma transição primeiro clique no botao `circulo-seta-circulo`, perto do botao de colocar estados, depois clique no primeiro estado (estado inicial) e arraste a seta que aparecer até um outro estado (estado final).
   - Você também pode adicionar uma transição para o mesmo estado clicando duas vezes no mesmo estado.

4. **Defina os estados marcados:**
   - Para definir os estados marcados, clique com **botão direito** no estado que você deseja marcar, selecione `Marking`, e por fim `accepting` (aceitação) ou `forbidden` (proibido).

5.  **Salve seu projeto:**
   - Quando terminar de criar seu autômato, vá para o menu `File` e selecione `Save` para salvar seu projeto.

## Guardas e Ações no Supremica

- As Guardas e Ações são elementos fundamentais na modelagem de sistemas de eventos discretos. As guardas são condições que devem ser satisfeitas para que uma transição ocorra, enquanto as ações são as operações que ocorrem quando uma transição é disparada.

- Para adicionar Guardas e Ações em um autômato, você precisa seguir os seguintes passos:
   1. Abra o software Supremica e crie um novo modelo de autômato.
   2. Adicione os estados e as transições do automato.
   3. Clique duas vezes na transição em que você deseja adicionar a guarda.
   4. Para adicionar a guarda coloque a condição a ser satisfeita para que a transição ocorra na primeira caixa de texto. A condição pode ser a de uma variável alcançar um determinado valor.
   5. Para adicionar uma Ação, adicione uma operação na segunda caixa de texto. Pode ser a atribuição de um valor a uma variável, por exemplo, e clique em `OK`.

## Autômato Finito Extendido no Supremica
   - Para criar uma automato estendido no supremica, crie um automato e adicione guardas, ações e variáveis, como descrito anteriormente.