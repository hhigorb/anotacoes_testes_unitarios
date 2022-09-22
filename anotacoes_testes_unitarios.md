## Testes Unitários:

### O que são testes unitários?

O teste unitário consiste em verificar o comportamento das menores unidades em sua aplicação.

Em linguagens orientadas a objetos, isso seria uma classe ou até mesmo um método, já em linguagens processuais uma função ou procedimento.

### O que faz um Teste Unitário ser um Teste Unitário?

Os testes unitários precisam funcionar isoladamente porque precisam funcionar rapidamente. Todo o conjunto de testes unitários de uma aplicação precisa funcionar em minutos, de preferência em segundos.

É por isso que os testes unitários não podem utilizar nenhum processo ou sistema externo. Nenhuma operação de E/S (input/output) de qualquer tipo (banco de dados, arquivo, console, rede) exceto o registro de falhas nos testes e talvez a leitura da configuração padrão de alternância de recursos no início de uma execução de teste.

Se seu código de teste (ou as bibliotecas que utiliza) fizer E/S ou acessar qualquer coisa fora de seu processo, não é um teste unitário, e sim um teste de integração.

### Qual é o Propósito dos Testes Unitários?

Muitos dizem que o objetivo dos testes unitários é validar que cada unidade de trabalho se comporta como projetada, esperada ou pretendida. E que você pode executar seus testes unitários toda vez que alguém faz uma mudança. Com apenas o apertar de um botão. 

Mas o verdadeiro propósito do teste unitário é fornecer-lhe feedback quase instantâneo sobre o projeto e a implementação de seu código.

A criação de testes unitários, ou melhor, a facilidade ou dificuldade com que você pode criá-los lhe diz exatamente o quão testável é seu código. O quão bem você o projetou. E se você escutá-los, ao invés de fazer gambiarras para superar qualquer dificuldade, todos ganham.

### Quais São os Benefícios dos Testes Unitários?

- Você economiza muito tempo nos testes de regressão.

- Você recebe um alerta sempre que, inadvertidamente, quebra um comportamento existente. Permitindo que você o enfrente imediatamente enquanto ainda está totalmente imerso no que você está trabalhando. Significa menos bugs escapando.

- Menos bugs escapando significa que você tem mais tempo para desenvolver valor.

- Trabalhando sem medo de quebrar o código existente sem saber, você possui mais recursos cognitivos preciosos. Significa que você será mais criativo e inovador, e capaz de criar soluções melhores.

- Você recebe documentação viva, respirando, nunca desatualizada – pelo menos quando você dá a cada teste unitário um nome significativo (mais sobre isso depois).

- Uma documentação sempre atualizada permite que você acelere os novos contratados.

- Trabalhando sem medo de quebrar o código existente sem saber, novos membros da equipe se tornam produtivos mais rapidamente.

- Menos bugs também significa que você reduzirá a carga da equipe de suporte e os liberará para se concentrar no sucesso do cliente ao invés de controlar os danos.
 
### Como Escrever Testes Unitários (Usando as Melhores Práticas)

Criar testes unitários é o mesmo que desenvolver qualquer código, mas há uma diferença. Você cria um código de aplicação funcional para resolver um problema para seus clientes. Você cria testes unitários para resolver os problemas que surgem no desenvolvimento do código da aplicação.

- Dê nomes de seus métodos de teste que o ajudem a entender os requisitos do código que você está testando sem ter que procurar em outro lugar. Escolha um dos vários modelos experimentados e testados que existem para isso e mantenha-se fiel a ele.

- Certifique-se de que um teste só tenha sucesso porque o código que ele testa está correto. Da mesma forma, assegure-se de que um teste só falha porque o código que ele testa está incorreto. Qualquer outra razão para o sucesso ou fracasso é enganar a si mesmo ou perseguir um buraco de coelho.

- Faça um esforço para criar mensagens curtas e significativas de falha que incluam parâmetros de teste relevantes. Há poucas coisas mais frustrantes do que “Esperado 5, mas encontrado 7” e ter que caçar o valor dos parâmetros para o método em teste.

- Certifique-se de que cada teste possa produzir os resultados corretos (sucesso ou falha) mesmo quando for o único teste que você executar.

Quando um teste depende de como outro teste mudou o ambiente (valores de variáveis, conteúdo de coleções, etc.), você terá dificuldade em acompanhar as condições iniciais para cada teste. Mais importante ainda, quando você obtiver resultados inesperados, você sempre se perguntará se as condições do teste ou o código de produção os causaram.

- Não otimizar a configuração do teste além do arquivo de origem de uma classe de teste. Mantenha uma classe de teste como um mundo para si mesma, independente das outras.
 
Use métodos de configuração e classes de utilidade aninhadas, se desejar, mas evite hierarquias de classes de teste e classes de utilidade geral. Isso evitará que você tenha que caçar através de diversas classes base ou unidades de classe de utilidade para encontrar os valores que um teste utiliza.

- Siga o padrão Arrange, Act, Assert. Marque cada parte com um comentário. A razão para seguir este padrão está no próximo ponto.

- Cada teste deve lidar apenas com:
    - Um arrange — Um cenário a ser testado (um “dado”).
    - Uma action — Um método para testar (um “quando”).
    - Um assert — Uma chamada para um método de verificação (um “então”).
 
### Armadilhas Comuns em Testes Unitários

Erros simples podem te fazer tropeçar seriamente. Pior ainda, eles podem te acalmar com uma falsa sensação de segurança.

Estes são os erros que você quer evitar

- Escrever testes sem afirmações.

Tal teste nunca falhará! Se não houver problema porque você está meramente verificando se não há exceções, faça isso explicitamente com uma afirmação e uma mensagem apropriada.

- Escrever mais de um teste de cada vez.

É uma indicação de que você está testando após o fato (em vez de uma abordagem de test-first), e está criando dores de cabeça para você mesmo ao acompanhar quais testes estão completos e devem ser bem sucedidos e quais testes falham por estarem incompletos.

- Não começar com um teste reprovado.

Quando você não começa com um teste reprovado, você não saberá se ele é bem sucedido porque você tem um erro em seu teste ou porque o código funcional está correto.

- Não executar testes frequentemente.

Idealmente, você deseja executar todos os testes unitários em cada etapa de um ciclo vermelho-verde-refatorar, quer você use isso com ou sem uma abordagem de test-first, como TDD e BDD.

- Escrever testes lentos.

Os testes lentos interrompem seu fluxo.

A propósito, não há problema em usar um framework de testes unitários (veja abaixo) para escrever testes (mais) lentos, mas eles não são testes unitários, e você quer mantê-los em um conjunto de testes separado.

- Tornar os testes dependentes de seu ambiente de testes.

Isso lhe dará dores de cabeça quando os testes falharem em um ambiente e forem bem-sucedidos em outro.
 
### Top melhores libs para Testes Unitários
 
- Robot
- PyTest
- Unittest
- DocTest
- Nose2
- Testify
