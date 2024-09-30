Otimização da Organização de Ondas de Produção com Limitação de Capacidade: Uma Abordagem Heurística gananciosa.

Introdução

A organização eficiente de ondas de produção em ambientes industriais é um desafio que exige a alocação otimizada de itens em lotes de produção, respeitando limitações de capacidade. Esse problema surge em fábricas, centros de distribuição e operações logísticas, onde a otimização de recursos e a minimização de complexidade são essenciais para garantir produtividade e redução de custos.

Neste projeto, buscamos resolver o problema de organização de itens (produtos) em caixas ou lotes de produção, respeitando uma capacidade máxima de 2000 peças por lote, utilizando uma metodologia heurística gulosa. A heurística gulosa foi escolhida pela sua simplicidade e eficiência computacional, garantindo soluções rápidas, mesmo em problemas de grande escala, sem necessariamente garantir a solução ótima, mas fornecendo boas soluções em um tempo viável.

Motivação

Resolver o problema de organização de ondas de produção utilizando métodos exatos pode ser computacionalmente muito caro, especialmente quando o número de itens e caixas é grande. Métodos exatos, como a programação linear inteira, têm a vantagem de garantir a solução ótima, porém, seu tempo de execução aumenta exponencialmente com o tamanho do problema. Heurísticas gulosas são uma alternativa prática para lidar com problemas dessa magnitude, oferecendo soluções rápidas e satisfatórias em cenários reais, onde as decisões precisam ser tomadas rapidamente.

O uso de uma abordagem heurística gulosa visa minimizar a dispersão dos itens em múltiplas ondas, otimizando o uso da capacidade disponível em cada lote e organizando os itens de forma a reduzir a complexidade do processo de produção.

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

