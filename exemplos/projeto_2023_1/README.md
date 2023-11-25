# Sistema de Manufatura Com Veículos Autoguiados

## Descrição
Neste projeto, foi modelado um sistema composta por várias etapas de produção, máquinas e veículos autoguiados para transportar itens entre as etapas. O objetivo é otimizar a produção, 
garantindo que os itens se movam eficientemente de uma máquina para outra, de acordo com a capacidade das máquinas, veículos e buffers.

## Componentes do Sistema
1. **Máquinas de Prodção (2x):** Cada máquina tem uma capacidade máxima de processamento e pode estar sujeita a falhas não controláveis, como quebras ou atrasos imprevistos.
   
2. **Veículos Autoguiados (2x):** Veículos autoguiados são usados para transportar os itens entre as máquinas. Eles têm a capacidade de alterar suas rotas dinamicamente.
   
3. **Buffer (1x):** Parte do sistema usado para armazer itens produzidos entre as máquinas.
   
4. **Itens (3x por ciclo):**  Os itens que precisam ser produzidos são transportados entre as máquinas e podem ser armazenados nos buffers.
   
## Eventos Não Controláveis
1. **Quebra das Máquinas:** Uma máquina pode quebrar inesperadamente, interrompendo a produção;
   
2. **Finalização de Processos:** Como há o a possibilidade de quebra inesperada das máquinas, a finalização dos processos, que dependem das peças vinda das máquinas, também se tornarão não controláveis.

## Estratégias de Controle Utilizadas: 
1. Rota Dinâmica do Veículo Autoguiado.
2. Gerenciamento de Prioridades na Entrega das Peças.
   
## Condições finais do projeto:
1. Sistema é **não bloqueante.**
2. Sistema é **controlável.**
3. Sistema é **livre de deadlock.**

## Modelo: 
O modelo é composto por 3 dos 4 tipos de autômatos disponíveis no Supremica. Sendo, 
* 5x Plantas: Part_input, Maq_01, Maq_02, AGV_01, AGV_02.
* 1x Requerimento: Buffer_Zone_01to02.
* 1x Supervisor.
  
Além de 5 variáveis, componente explicado no seguinte README: [Tutorial Supremica](https://github.com/kyllercg/tutorial-supremica/blob/main/README.md).

Variáveis: 
* maq01_items: Suporta 1 item, representa se a máquina está ocupada ou não.
* maq02_items: Suporta 1 item, representa se a máquina está ocupada ou não.
* agv01_items: Suporta 1 item, representa se o veículo está ocupada ou não.
* agv02_items: Suporta 1 item, representa se o veículo está ocupada ou não.
* bfz01_02_item_qty: Suporta 3 items, representa quantos itens há no buffer.

## Considerações
Este projeto aborda desafios práticos encontrados em ambientes de produção real e demonstra como o controle supervisório pode ser usado para melhorar a eficiência e a adaptabilidade do sistema em resposta a eventos imprevisíveis.

