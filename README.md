# Projeto-Strategy

- Intenção:

Strategy é um padrão de design comportamental que permite definir uma família de algoritmos, colocar cada um deles em uma classe separada e tornar seus objetos intercambiáveis.
Defina uma família de algoritmos, encapsule cada um e torne-os intercambiáveis. A estratégia permite que o algoritmo varie independentemente dos clientes que utilizam.
Capture a abstração em uma interface, enterre os detalhes de implementação em classes derivadas.

- Implementação:

Na classe de contexto, identifique um algoritmo que está sujeito a mudanças frequentes. Também pode ser uma condicional massiva que seleciona e executa uma variante do mesmo algoritmo em tempo de execução.

Declare a interface de estratégia comum a todas as variantes do algoritmo.

Um por um, extraia todos os algoritmos em suas próprias classes. Todos eles devem implementar a interface da estratégia.

Na classe de contexto, adicione um campo para armazenar uma referência a um objeto de estratégia. Fornece um setter para substituir os valores desse campo. O contexto deve funcionar com o objeto de estratégia apenas por meio da interface de estratégia. O contexto pode definir uma interface que permite à estratégia acessar seus dados.

Os clientes do contexto devem associá-lo a uma estratégia adequada que corresponda à maneira como eles esperam que o contexto execute sua tarefa principal.

- Estrutura:

A entidade Interface pode representar uma classe base abstrata ou as expectativas de assinatura do método pelo cliente. No primeiro caso, a hierarquia de herança representa o polimorfismo dinâmico. No último caso, a entidade Interface representa o código do modelo no cliente e a hierarquia de herança representa o polimorfismo estático.

![alt text](https://sourcemaking.com/files/v2/content/patterns/Strategy_.png)

- Exemplo

Uma Strategy define um conjunto de algoritmos que podem ser usados alternadamente. Os meios de transporte para um aeroporto são um exemplo de Strategy. Existem várias opções, como dirigir o próprio carro, pegar um táxi, um ônibus para o aeroporto, um ônibus urbano ou um serviço de limusine. Para alguns aeroportos, metrôs e helicópteros também estão disponíveis como meio de transporte para o aeroporto. Qualquer um desses meios de transporte leva o viajante ao aeroporto e pode ser usado de forma intercambiável. O viajante deve escolher a Strategy com base nas compensações entre custo, conveniência e tempo.

![alt text](https://sourcemaking.com/files/v2/content/patterns/Strategy_example1.png)
