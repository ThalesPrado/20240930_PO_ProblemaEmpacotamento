Otimização da Organização de Ondas de Produção com Limitação de Capacidade: Um Modelo Baseado em Programação Linear Inteira

Introdução

A organização eficiente de processos de produção é fundamental para garantir alta produtividade e redução de custos em ambientes industriais. Um dos desafios mais comuns em fábricas e centros de distribuição é organizar produtos em "ondas de produção" (batches) de forma a otimizar o uso de recursos e minimizar os custos operacionais.

Neste projeto, estudamos um problema clássico de organização de ondas de produção, no qual itens (produtos) devem ser alocados em caixas (ou lotes) de produção respeitando uma capacidade máxima de 2000 peças por lote. O objetivo é organizar esses produtos em um número mínimo de ondas, de modo que cada item apareça no menor número de ondas possível. A solução proposta será baseada em um modelo de programação linear inteira (PLI), que visa a otimização do processo, respeitando restrições de capacidade e garantindo que cada item seja processado ao menos uma vez.

Motivação

A minimização da quantidade de ondas de produção é essencial para evitar a dispersão de itens em diferentes lotes, o que pode aumentar o tempo de setup de máquinas, custos de logística interna e a complexidade de planejamento. Além disso, lotes otimizados tendem a melhorar a utilização da capacidade produtiva, reduzindo o tempo ocioso das máquinas e maximizando o throughput.

Esse problema é comum em indústrias de manufatura, logística e distribuição, onde os recursos são limitados e a otimização de lotes é uma ferramenta chave para ganhos operacionais. Nosso projeto se concentra no desenvolvimento de um modelo matemático preciso, que pode ser aplicado a diversos setores industriais.

1. Objetivo: Minimização das Ondas de Produção
O objetivo principal é minimizar o número total de ondas, onde cada item deve ser alocado de maneira a aparecer no menor número possível de ondas:

<img width="161" alt="Screenshot 2024-09-30 213034" src="https://github.com/user-attachments/assets/c9089106-31c4-4585-aa28-756a8659cf4e">

K é o conjunto de caixas
J é o conjunto de ondas de produção
Zkj indica se o item K está alocado à onda J

2. Restrições
Para que o modelo seja viável, precisamos garantir que diversas condições sejam atendidas. As principais restrições são descritas a seguir:

(1) Cada item deve ser alocado a exatamente uma onda:

<img width="128" alt="Screenshot 2024-09-30 213358" src="https://github.com/user-attachments/assets/b9b4347d-b07c-4de8-9e49-854db902eecc">

Esta equação garante que cada item i é alocado a exatamente uma onda j e o valor de Xij = 1 garante que o item i pertence a onda j.

(2) Um item só pode ser alocado a uma onda se essa onda for ativada

<img width="142" alt="3" src="https://github.com/user-attachments/assets/3da702da-e68d-49f5-83bf-387a472dc25b">

Yi é uma variável binária que indica se a onda j foi ativada. Isso implica que um item i só pode ser alocado à onda j se esse onda de fato estiver ativa.

(3) A alocação de caixas segue a mesma lógica da alocação de itens:

<img width="164" alt="4" src="https://github.com/user-attachments/assets/cb17d5f4-763e-4535-a46e-feaa53210cd0">

Aqui, asseguramos que a alocação dos itens i implicam na ativação do lote k na onda j.

(4) Limitação de capacidade por onda:

Essa restrição assegura que a quantidade total de peças alocadas a uma determinada onda j não exceda a capacidade c, que que é definida como 2000 peças. pi representa a quantidade de peças do item i

3. Variáveis de Decisão

As variáveis de decisão são binárias, indicando se os itens e as ondas foram ativados ou não:

Xij {0,1} -> Indica se o item i está presente na onda j
Yi {0,1} -> Indica se a onda j está ativada
Zkj {0,1} -> Indica se a caixa k foi alocada à onda j

4. Resultados Esperados

Com base na aplicação do modelo, esperamos obter um número mínimo de ondas de produção sem comprometer a capacidade dos lotes e sem fragmentar itens desnecessariamente. Isso resultará em uma melhoria significativa na eficiência operacional e na utilização de recursos.

Além disso, o modelo fornecerá insights sobre como diferentes configurações de produtos e caixas impactam a organização das ondas, possibilitando ajustes dinâmicos na programação de produção.

5. Resultados Obtidos

<img width="470" alt="5" src="https://github.com/user-attachments/assets/9daf143f-51eb-4a3d-8e4c-c517be0121bc">


<img width="476" alt="6" src="https://github.com/user-attachments/assets/59d68f5d-b5af-4389-ba25-cee5d975535d">

