# Introdução ao TCP/IP, Camadas e Protocolos

Criado em: 28 de maio de 2024 21:32

A arquitetura TCP/IP surgiu na década de 1970, em um projeto militar que foi avançando para o centro acadêmico nas pesquisas cientificas. Depois foi implementada nas grandes empresas até chegar nas residências. Mas afinal, do que se trata esse modelo? Pense que, antes do surgimento da internet na qual conhecemos hoje, principalmente em momentos de guerra, era necessário um meio de comunicação. Daí surgiu este projeto, que é utilizado até hoje para transferência de dados. 

Antes de tudo, vale ressaltar que este artigo é um resumo a grosso modo para não entrar em cálculos complexos, pois o intuito é fazer uma introdução do modelo TCP/IP e ao entendimento de como a informação é compartilhada. 

Neste tema, você precisa saber o que é uma camada no processo de transmissão. Para isso, vou fazer uma analogia para deixar bem claro o que significa na área de redes, pois cada camada é um processo diferente e é muito importante saber diferenciá-las. A cebola, por exemplo, é composta por várias camadas. Digamos que a casca é a camada de aplicação e, quando você começa a descascá-la, vai diminuindo até chegar ao núcleo. Em redes, a camada mais baixa é a camada física, onde passam os impulsos elétricos e que é a base sobre a qual a rede é construída. Nesse processo, a informação precisa ser fragmentada em pacotes para passar por essas camadas. Do transmissor para o receptor, ela é reduzida em pequenos quadros e, quando chega ao destino, é necessário reestruturar os pacotes. Assim, a cebola precisa voltar com suas camadas até chegar à casca novamente.

Mas como a informação chega até você? Como o sistema não erra o destino? Como o impulso elétrico, representado como sinal analógico, pode ser convertido em bits digitais? E como funciona todo o sistema para apresentar a informação ao usuário? Existe todo um processo para chegar a outra máquina, e tudo isso é descrito na área de redes, onde há vários serviços e protocolos envolvidos.

O TCP/IP é uma arquitetura de redes baseada em protocolos e é separada por camadas, semelhante ao modelo OSI. Ambos têm funções semelhantes, porém o modelo OSI possui 7 camadas, enquanto o TCP/IP possui apenas 4 camadas.

Abaixo está um exemplo do modelo TCP/IP, onde o Usuário 1 envia a informação para o Usuário 2. A informação que está na camada de aplicação vai "descendo" até a camada física e, no local do Usuário 2, a informação chega na camada física e vai "subindo" até a camada de aplicação.

---

**Usuário1 → Aplicação → Transporte → Rede → Física** 

**Física  → Rede → Transporte → Aplicação → Usuário2**

---

Caso haja algum problema no envio de dados, a camada de rede verificará quais quadros não foram enviados e os enviará novamente. Isso dependerá de alguns protocolos que serão abordados em outro artigo.

Essa estrutura de rede foi feita por camadas com o objetivo de simplificar a identificação e correção de erros. Cada camada tem um tipo de erro específico, o que agiliza o processo de correção. Partindo do princípio de que nenhuma camada está livre de erros, é necessário utilizar vários protocolos para minimizar a dispersão de dados.

Os protocolos foram criados para garantir a compatibilidade ou padronização entre diversos fornecedores e marcas, permitindo assim a transferência de dados.

Entretanto, podemos notar que uma camada depende da outra. Cada uma tem a função de fornecer serviço à camada superior. A camada física fornece serviço para a camada de rede e assim sucessivamente, até a informação chegar à última camada.

Em outro artigo será abordado exclusivamente camada por camada para saber detalhadamente como cada uma funciona. 

Sandro Gomes

Cientista da computação.

Referências:
TANENBAUM, Andrew S.; WETHERALL, David J. **Redes de Computadores**. 5. ed. São Paulo: Pearson, 2011.

ELIAS, Glêdson; LOBATO, Luiz Carlos. **Arquitetura e Protocolos de Rede TCP-IP**. Rio de Janeiro: Escola Superior de Redes, 2013.