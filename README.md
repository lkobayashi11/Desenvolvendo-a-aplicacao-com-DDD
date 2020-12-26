## Desenvolvendo com DDD (Domain Driven Design)

 

Neste projeto, Alexandre Daccas (Arquiteto de Software da Avanade) , explica o conceito de DDD e suas aplicações no desenvolvimento de software.

Utilizando o código do projeto Aurora, desenvolvido por Alex Alves, Daccas exibe de forma prática, como o DDD torna a codificação mais organizada, modularizada e independente.



##### O que é DDD ou Domain Driven Design?

Domain Driven Design significa Projeto Orientado a Domínio. O conceito surgiu do livro escrito por Eric Evans publicado em 2003. 

Domain Driven Design “’é um conjunto de princípios com foco em domínio, exploração de modelos de formas criativas e definir e falar a linguagem Ubíqua, baseado no contexto delimitado.”

 

##### Domínio

Domínio é o coração do negócio,  baseado em um conjunto de ideias, conhecimento e processos de negócio. É a razão do negócio existir. Sem o domínio todo o sistema, todos os processos auxiliares, não servirão para nada.

Se uma empresa existe, é porque possui um core business e, normalmente, esse core business é composto pelo domínio principal.

Resumindo, sempre que se falar em domínio, estaremos falando da razão daquele software existir. Sem aquele ponto principal, não há razão para o desenvolvimento do software.

Quando falamos em DDD – Domain Driven Design, não falamos apenas em desenvolver um software, mas sim em entender a modelagem do projeto como um todo.



##### Linguagem Ubíqua

O DDD preza que os desenvolvedores façam parte do processo, entendendo o negócio e todos os seus modelos nos diferentes ângulos e não somente participando de reuniões com especialistas.

Fazendo um relacionamento com o mundo dos serviços, o novo perfil dos desenvolvedores faz com que o time participe de todo o processo, desde o levantamento de requisitos até o contato com o Domain Expert. Antigamente, o desenvolvedor apenas codificava

Um dos pontos mais importantes do DDD, onde 99% das pessoas acabam ignorando, que é falar e extrair a linguagem Ubíqua.

Domain-Driven Design é, antes de tudo, comunicação. Especialistas do domínio (usuários, analistas e outros especialistas da área), juntamente com os desenvolvedores e arquitetos trabalham de mãos dadas com um objetivo em comum: construir software guiado pelo domínio para atender as necessidades do cliente.

Para fazer isso, em primeiro lugar, é necessário que todos usem uma linguagem em comum e que não haja tradução na comunicação entre os membros do time.

Linguagem Ubíqua é a linguagem falada no dia dia, no contexto da empresa. É a linguagem que utiliza as terminologias da realidade do negócio.

A ideia principal é você fazer a ligação da Linguagem Ubíqua entre os Experts no Negócio e os desenvolvedores. Quando eles conseguem definir quais são os termos que eles mais irão utilizar, essa extração fará toda a diferença no processo de desenvolvimento e comunicação na aplicação. Quando utilizamos a Linguagem Ubíqua é muito importante que esteja tudo organizado e extraído.



DDD pode ser visto por alguns como a volta da orientação a objetos. Quando se fala em Orientação a Objetos pensa-se logo em classes, heranças, polimorfismo, encapsulamento. Mas a essência da Orientação a Objetos também tem coisas como:

- Alinhamento do código com o negócio: o contato dos desenvolvedores com os especialistas do domínio é algo essencial quando se faz DDD (o pessoal de métodos ágeis já sabe disso faz tempo);
- Favorecer reutilização: os blocos de construção, que veremos adiante, facilitam aproveitar um mesmo conceito de domínio ou um mesmo código em vários lugares;
- Mínimo de acoplamento: Com um modelo bem feito, organizado, as várias partes de um sistema interagem sem que haja muita dependência entre módulos ou classes de objetos de conceitos distintos;
- Independência da Tecnologia:  DDD não foca em tecnologia, mas sim em entender as regras de negócio e como elas devem estar refletidas no código e no modelo de domínio. Não que a tecnologia usada não seja importante, mas essa não é uma preocupação de DDD.

 

**Blocos de construção do Model Driven Design (MDD)**

Uma vez que decidimos criar um modelo usando MDD, precisamos, inicialmente, isolar o modelo de domínio das demais partes que compõem o sistema. Essa separação pode ser feita utilizando-se uma arquitetura em camadas, que dividirá nossa aplicação em partes:

Aplicação – essa camada não possui lógica de negócio. Ela é apenas uma camada fina, responsável por conectar a Interface de Usuário às camadas inferiores;

Domínio – representa os conceitos, regras e lógicas de negócio. Todo o foco de DDD está nessa camada. Nosso trabalho, daqui para frente, será aperfeiçoar e compreender profundamente essa parte;

Infra-estrutura – fornece recursos técnicos que darão suporte às camadas superiores. São normalmente as partes de um sistema responsáveis por persistência de dados, conexões com bancos de dados, envio de mensagens por redes, gravação e leitura de discos, etc.



Depois de dividirmos o sistema em camadas, nos preocuparemos apenas com a camada de domínio. Para modelar essa parte, utilizamos alguns Padrões propostos em DDD. Esses padrões são chamados de blocos de construção e serão utilizados para representar nosso modelo abstrato. Esses blocos podem ser:

- Entidades: classes de objetos que necessitam de uma identidade. Normalmente são elementos do domínio que possuem ciclo de vida dentro de nossa aplicação.
- Objetos de Valores: objetos que só carregam valores, mas que não possuem distinção de identidade. 
- Agregados: compostos de Entidades ou Objetos de Valores que são encapsulados numa única classe. O Agregado serve para manter a integridade do modelo. 
- Fábricas:  classes responsáveis pelo processo de criação dos Agregados ou dos Objetos de Valores. 
- Serviços: classes que contém lógica de negócio, mas que não pertence a nenhuma Entidade ou Objetos de Valores. 
- Repositórios: classes responsáveis por administrar o ciclo de vida dos outros objetos, normalmente Entidades, Objetos de Valor e Agregados. Os repositórios são classes que centralizam operações de criação, alteração e remoção de objetos. 
- Módulos: abstrações que têm por objetivos agrupar classes por um determinado conceito do domínio. 

 

**Referências**

https://fullcycle.com.br/domain-driven-design/

http://www.agileandart.com/2010/07/16/ddd-introducao-a-domain-driven-design/