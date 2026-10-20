
### Atividade sobre agentes inteligentes
Aula 20/10/2026 | Professora Kadidja Valéria | Inteligência artificial
**Disciplina:**  Linguagens Formais e Autômatos | Ciência da Computação
**Estudante:**  Paulo Henrique de Melo Loiola |  **Turma:**  Ciência da Computação - N1

Realize os exercícios 2.3, 2.4 e 2.5 do Capítulo 2 sobre agentes inteligentes. Analise a racionalidade, descreva ambientes de tarefa por meio do modelo PEAS e explique os conceitos com suas próprias palavras. Utilize o capítulo disponibilizado e justifique suas respostas.
**Modalidade sugerida:**  individual com consulta.  **Tempo estimado:**  2h30.  **Prazo:**  conforme orientação da professora.

#### Preparação
Leia os tópicos sobre racionalidade, ambientes e estrutura dos agentes, especialmente a Seção 2.3.2.

#### Exercício 2.3
Para cada afirmação, indique V ou F, justifique e forneça exemplo ou contraexemplo. Explicite as hipóteses utilizadas.

##### a. Um agente que detecta apenas informações parciais sobre o estado não pode ser perfeitamente racional.
*  Julgamento: F
*  Justificativa: A racionalidade depende da maximização do desempenho esperado com base na sequência de percepções recebida até o momento e no conhecimento prévio do agente, e não de ter acesso a informações perfeitas ou completas do ambiente. Exigir informação completa seria exigir onisciência, o que é distinto da racionalidade.
*  Exemplo ou contraexemplo: Um agente jogador de pôquer ou um robô móvel com sensores limitados que escolhe a ação que maximiza a utilidade esperada com base nas probabilidades calculadas a partir das percepções parciais é perfeitamente racional.

##### b. Existem ambientes de tarefa nos quais nenhum agente reativo puro pode comportar-se racionalmente.
*  Julgamento: V
*  Justificativa: Agentes reativos puros tomam decisões baseando-se apenas na percepção do instante atual, sem manter histórico de percepções ou estado interno. Em ambientes parcialmente observáveis, a percepção atual não fornece dados suficientes para distinguir estados que exigem ações diferentes, levando o agente a loops infinitos ou decisões incorretas.
*  Exemplo ou contraexemplo: Um aspirador de pó em um ambiente de dois quadrados desprovido de sensor de posição (possuindo apenas sensor de sujeira) que percebe [Limpo] entrará em loop infinito se sua regra estática for mover para a esquerda quando estiver no quadrado A.

##### c. Existe um ambiente de tarefa em que todo agente é racional.
*  Julgamento: V
*  Justificativa: A racionalidade é avaliada em relação a uma medida de desempenho. Se a medida de desempenho de um ambiente atribuir o mesmo valor para todas as ações executadas em qualquer estado, qualquer agente (independentemente das suas escolhas) alcançará o desempenho máximo esperado e será racional.
*  Exemplo ou contraexemplo: Um ambiente de tarefa no qual a medida de desempenho atribua pontuação constante (como 10 pontos) para qualquer ação realizada pelo agente.

##### d. A entrada para o programa de agente é a mesma que a entrada para a função de agente.
*  Julgamento: F
*  Justificativa: A função de agente é uma descrição matemática abstrata que recebe como entrada a sequência ou histórico completo de percepções acumuladas até o momento. Em contraste, o programa de agente é uma implementação concreta que recebe como entrada física apenas a percepção do instante atual enviada pelos sensores.
*  Exemplo ou contraexemplo: No mundo do aspirador de pó, a função de agente recebe a sequência inteira de percepções como `[[A, Limpo], [A, Sujo], [B, Limpo]]`, enquanto o programa do agente recebe unicamente o elemento atual `[B, Limpo]`.

##### e. Toda função de agente é implementável por uma combinação de programa/máquina.
*  Julgamento: F
*  Justificativa: Existem funções de agente abstratas que exigem tabelas infinitas ou impraticavelmente gigantescas que excedem a capacidade de memória física de qualquer computador no universo observável. Além disso, existem funções de agente não computáveis na teoria da computação.
*  Exemplo ou contraexemplo: Uma função de agente de direção automatizada cuja tabela de mapeamento exige mais de \\(10^{250.000.000.000}\\) entradas para uma hora de condução não pode ser armazenada em nenhuma máquina física existente.

##### f. Suponha que um agente selecione sua ação uniformemente ao acaso do conjunto de ações possíveis. Existe um ambiente de tarefa determinista em que esse agente é racional.
*  Julgamento: V
*  Justificativa: Se em um ambiente determinista todas as ações possíveis produzirem o mesmo valor máximo de desempenho, a escolha aleatória uniforme garantirá o desempenho esperado ótimo, satisfazendo a definição de racionalidade.
*  Exemplo ou contraexemplo: Um ambiente determinista no qual a medida de desempenho concede 1 ponto para qualquer ação executada ("Mover Esquerda" ou "Mover Direita"), sem penalidades.

##### g. É possível para um dado agente ser perfeitamente racional em dois ambientes de tarefa distintos.
*  Julgamento: V
*  Justificativa: A racionalidade depende de maximizar o desempenho esperado para uma dada sequência de percepções e conhecimento prévio. Se dois ambientes distintos possuírem a mesma dinâmica e estrutura de recompensas em relação às percepções do agente, o mesmo programa de agente será racional em ambos.
*  Exemplo ou contraexemplo: O programa de um agente aspirador de pó reativo é racional tanto em um ambiente de dois quadrados em um laboratório quanto em um ambiente réplica idêntico em uma casa.

##### h. Todo agente é racional em um ambiente não observável.
*  Julgamento: F
*  Justificativa: Em um ambiente não observável (sem sensores), o agente racional deve utilizar seu conhecimento prévio \\(a\ priori\\) para executar uma sequência fixa otimizada de ações. Um agente que tome ações aleatórias prejudiciais sem considerar o conhecimento prévio não será racional.
*  Exemplo ou contraexemplo: Em um mundo de aspirador inobservável onde se sabe que ambos os quadrados estão sujos, um agente que opte por ficar parado sem aspirar é irracional.

##### i. Um agente jogador de pôquer perfeitamente racional nunca perde.
*  Julgamento: F
*  Justificativa: O pôquer é um ambiente estocástico e parcialmente observável. A racionalidade maximiza o desempenho esperado (utilidade esperada) e não garante a perfeição no resultado real. Um agente racional pode tomar a decisão probabilística ótima e ainda assim perder devido ao azar na distribuição das cartas ocultas do oponente.
*  Exemplo ou contraexemplo: Um jogador de pôquer que entra na jogada com a melhor mão possível probabilística (como um par de Ás) toma a decisão perfeitamente racional, mas pode perder a rodada se o oponente acertar uma combinação improvável no final.

#### Exercício 2.4
Para cada caso, delimite o agente, preencha o PEAS e justifique todas as classificações. Considere Titã como cenário hipotético do exercício.

##### Caso 1 — Jogar futebol.
*  Agente analisado: Robô jogador de futebol.
*  Objetivo e hipóteses: Marcar gols e vencer partidas respeitando as regras do jogo, em campo com outros jogadores em movimento.
*  P — Medida de desempenho: Gols marcados, vitórias, passes certos, minimização de gols sofridos e ausência de infrações.
*  E — Ambiente: Campo de futebol, bola, colegas de equipe, oponentes, juiz, traves e condições climáticas.
*  A — Atuadores: Motores para articulação das pernas/rodas (chutar e correr), tronco e dispositivo de comunicação por voz.
*  S — Sensores: Câmeras de visão computacional, acelerômetros, giroscópios, encoders de roda e microfones.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Parcialmente observável | O agente não enxerga todo o campo simultaneamente nem observa os estados mentais dos adversários. |
| Número de agentes | Multiagente (cooperativo e competitivo) | Inclui colegas de equipe cooperando e oponentes competindo para maximizar metas opostas. |
| Previsibilidade | Estocástico | O movimento da bola, atrito do gramado e reações de outros jogadores possuem incerteza probabilística. |
| Dependência entre decisões | Sequencial | Cada decisão de passe ou posicionamento afeta as situações de jogo futuras a longo prazo. |
| Mudança durante a decisão | Dinâmico | O ambiente e os outros jogadores continuam se movendo enquanto o agente computa sua ação. |
| Natureza dos elementos | Contínuo | Posições, velocidades, tempo, força do chute e ângulos variam em uma escala contínua. |
| Conhecimento do funcionamento | Conhecido | As regras do futebol e as leis da física que regem os movimentos são conhecidas \\(a\ priori\\). |

##### Caso 2 — Explorar os oceanos subterrâneos de Titã.
*  Agente analisado: Sonda/Submarino robótico explorador autônomo.
*  Objetivo e hipóteses: Mapear o oceano subterrâneo e coletar amostras químicas/biológicas mantendo a integridade do veículo em ambiente extremo.
*  P — Medida de desempenho: Área oceânica mapeada, volume e relevância das amostras coletadas, preservação da sonda e autonomia energética.
*  E — Ambiente: Oceano de fluido líquido sob a crosta de gelo de Titã, escuridão, correntes aquáticas, relevo rochoso e alta pressão.
*  A — Atuadores: Propulsores marítimos, braço mecânico de coleta, broca de perfuração, sistema de flutuabilidade e transmissor sonar/rádio.
*  S — Sensores: Sonar de varredura, câmeras infravermelhas, sensores de pressão e temperatura, espectrômetro e giroscópio.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Parcialmente observável | A escuridão e a turbidez do fluido limitam o alcance dos sensores no oceano. |
| Número de agentes | Agente único | Não há outros agentes inteligentes conhecidos operando no ambiente submarino de Titã. |
| Previsibilidade | Estocástico | Correntes marítimas imprevistas e obstáculos ocultos introduzem incertezas nos resultados. |
| Dependência entre decisões | Sequencial | O consumo de energia e rotas escolhidas afetam diretamente a capacidade de sobrevivência futura. |
| Mudança durante a decisão | Dinâmico | As correntes aquáticas e a posição da sonda mudam enquanto o agente delibera. |
| Natureza dos elementos | Contínuo | Pressão, temperatura, velocidade, localização espacial e tempo variam continuamente. |
| Conhecimento do funcionamento | Desconhecido | O ambiente aquático de Titã não é totalmente conhecido \\(a\ priori\\), exigindo exploração e aprendizado. |

##### Caso 3 — Comprar livros usados de IA na Internet.
*  Agente analisado: Agente de software comprador (softbot de e-commerce).
*  Objetivo e hipóteses: Localizar e comprar edições específicas de livros de IA pelo menor preço total, em lojas e sebos virtuais.
*  P — Medida de desempenho: Minimização do custo total (preço do livro + frete), boa conservação do livro e rapidez na entrega.
*  E — Ambiente: Internet, sites de e-commerce, APIs de lojas virtuais, bancos de dados e serviços de frete.
*  A — Atuadores: Envio de mensagens HTTP/API, preenchimento de campos de formulários e confirmação digital de compra.
*  S — Sensores: Leitura do código HTML/JSON de páginas web, preços listados, disponibilidade de estoque e respostas HTTP.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Parcialmente observável | O estado físico real de conservação do livro e a confiabilidade do vendedor não são diretamente observáveis antes da compra. |
| Número de agentes | Multiagente (competitivo) | Compete com outros compradores por estoques limitados e interage com sistemas de precificação. |
| Previsibilidade | Estocástico | Variações de preço repentinas, esgotamento de estoque e atrasos de entrega possuem comportamento incerto. |
| Dependência entre decisões | Sequencial | Realizar uma compra consome o orçamento disponível e altera as opções de compra subsequentes. |
| Mudança durante a decisão | Dinâmico | Preços e estoques podem ser alterados por outros usuários enquanto o agente analisa os dados. |
| Natureza dos elementos | Discreto | Preços, edições de livros, número de páginas e cliques em botões são variáveis discretas. |
| Conhecimento do funcionamento | Conhecido | As regras do comércio eletrônico e os protocolos de navegação web são conhecidos \\(a\ priori\\). |

##### Caso 4 — Jogar uma partida de tênis.
*  Agente analisado: Robô tenista autônomo.
*  Objetivo e hipóteses: Vencer a partida rebatendo a bola dentro da quadra adversária segundo as regras do tênis.
*  P — Medida de desempenho: Pontos, games e sets conquistados, precisão dos saques/devoluções e minimização de erros.
*  E — Ambiente: Quadra de tênis, rede, bola, oponente, juiz de partida e vento/iluminação.
*  A — Atuadores: Motores de deslocamento nas pernas e atuadores articulados no braço/raquete.
*  S — Sensores: Câmeras de visão estereoscópica de alta velocidade, sensores de impacto na raquete e giroscópios.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Parcialmente observável | O efeito de rotação interno da bola e a intenção tática imediata do oponente são parcialmente ocultos. |
| Número de agentes | Multiagente (competitivo) | O adversário atua ativamente para maximizar sua medida de desempenho, minimizando a do agente. |
| Previsibilidade | Estocástico | Vento, quiques na linha e imperfeições na bola introduzem aleatoriedade ao resultado das ações. |
| Dependência entre decisões | Sequencial | O tipo e a direção do golpe aplicado condicionam o posicionamento futuro de ambos os jogadores. |
| Mudança durante a decisão | Dinâmico | A bola se move pelo ar continuamente enquanto o programa de agente calcula sua resposta. |
| Natureza dos elementos | Contínuo | Posições espaciais, velocidade da bola, força da batida e tempo são variáveis contínuas. |
| Conhecimento do funcionamento | Conhecido | As regras da partida e as leis físicas de movimento parabólico e colisão são conhecidas. |

##### Caso 5 — Praticar tênis contra uma parede.
*  Agente analisado: Robô tenista praticando rebatidas contra um paredão.
*  Objetivo e hipóteses: Manter uma sequência contínua de devoluções rebatendo a bola em um paredão rígido para aperfeiçoar a precisão.
*  P — Medida de desempenho: Quantidade de rebatidas consecutivas sem deixar a bola cair e precisão do ponto de impacto na parede.
*  E — Ambiente: Parede vertical rígida, piso da quadra, bola de tênis e vento local.
*  A — Atuadores: Motores das pernas para deslocamento e atuadores do braço/raquete para batida.
*  S — Sensores: Câmeras de vídeo, acelerômetros, giroscópios e microfone de impacto.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Completamente observável | O agente observa diretamente a posição da bola, sua trajetória e a parede por inteiro. |
| Número de agentes | Agente único | A parede é um objeto passivo que obedece às leis físicas, não um agente com objetivos concorrentes. |
| Previsibilidade | Estocástico | Imperfeições no piso/parede e pequenas rajadas de vento podem alterar sutilmente o quique da bola. |
| Dependência entre decisões | Sequencial | A força e a direção empregadas no golpe atual definem a velocidade e o ângulo do retorno da bola. |
| Mudança durante a decisão | Dinâmico | A bola continua voando em direção ao agente enquanto o programa decide a ação de deslocamento. |
| Natureza dos elementos | Contínuo | Posição no espaço, velocidade, tempo e forças variam continuamente. |
| Conhecimento do funcionamento | Conhecido | A física mecânica de colisão e a elasticidade são totalmente conhecidas pelo agente. |

##### Caso 6 — Realizar um salto de altura.
*  Agente analisado: Robô atleta de salto em altura.
*  Objetivo e hipóteses: Executar corrida de aproximação, impulsão e arqueamento para ultrapassar a fasquia na maior altura possível sem derrubá-la.
*  P — Medida de desempenho: Altura da fasquia ultrapassada com sucesso e minimização de falhas nas tentativas.
*  E — Ambiente: Pista sintética de corrida, suporte vertical com fasquia/sarrafo, colchão de amortecimento e vento.
*  A — Atuadores: Motores de alto desempenho nas pernas (impulsão) e atuadores de tronco/membros para arqueamento corporal.
*  S — Sensores: Telêmetro laser/LIDAR (distância do sarrafo), acelerômetros, giroscópios e câmeras de posição.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Completamente observável | A altura do sarrafo, a distância da pista e a posição do colchão são totalmente visíveis ao agente. |
| Número de agentes | Agente único | O salto é uma tentativa individual na qual nenhum outro agente interfere durante a execução. |
| Previsibilidade | Estocástico | Variações na aderência do piso e pequenas rajadas de vento introduzem incertezas na trajetória. |
| Dependência entre decisões | Sequencial | Os passos na corrida de aproximação determinam a velocidade e o ângulo de impulsão no salto final. |
| Mudança durante a decisão | Semidinâmico | O ambiente não se altera sozinho durante a preparação, mas o tempo computacional afeta o momento correto do salto. |
| Natureza dos elementos | Contínuo | Velocidade, ângulo de salto, trajetória parabólica e flexão corporal são contínuos. |
| Conhecimento do funcionamento | Conhecido | As regras do atletismo e as leis mecânicas e gravitacionais são conhecidas \\(a\ priori\\). |

##### Caso 7 — Participar de um leilão de um item, realizando lances.
*  Agente analisado: Agente de software comprador em leilão.
*  Objetivo e hipóteses: Arrematar o item leiloado pelo menor preço possível, sem ultrapassar o valor máximo de avaliação privada.
*  P — Medida de desempenho: Sucesso no arremate do item, maximização da margem de economia em relação ao limite e minimização de taxas.
*  E — Ambiente: Plataforma de leilão, leiloeiro, licitantes concorrentes e histórico de lances do item.
*  A — Atuadores: Envio digital de novo lance, confirmação de cobertura de oferta ou desistência do leilão.
*  S — Sensores: Monitoramento de mensagens do leiloeiro, lances concorrentes atuais e cronômetro.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Parcialmente observável | Os valores máximos e as estratégias privadas dos outros licitantes são informações ocultas. |
| Número de agentes | Multiagente (competitivo) | Outros licitantes competem diretamente para vencer o leilão, elevando os preços. |
| Previsibilidade | Estocástico | Os lances e comportamentos dos outros concorrentes não podem ser previstos com certeza. |
| Dependência entre decisões | Sequencial | Cada lance submetido altera o preço atual e condiciona as opções de lances futuros. |
| Mudança durante a decisão | Dinâmico | O cronômetro avança e outros licitantes podem enviar lances enquanto o agente analisa sua decisão. |
| Natureza dos elementos | Discreto | Os lances ocorrem em incrementos monetários discretos e em instantes de tempo discretos. |
| Conhecimento do funcionamento | Conhecido | As regras formais do leilão (incrementos mínimos e prazo de encerramento) são conhecidas \\(a\ priori\\). |

##### Opções para classificação
*   **Observabilidade:**  Completamente observável, parcialmente observável ou não observável.
*   **Número de agentes:**  Agente único ou multiagente; indique cooperação ou competição quando pertinente.
*   **Previsibilidade:**  Determinístico ou estocástico; considere a influência estratégica de outros agentes.
*   **Dependência entre decisões:**  Episódico ou sequencial.
*   **Mudança durante a decisão:**  Estático, dinâmico ou semidinâmico.
*   **Natureza dos elementos:**  Discretos, contínuos ou combinação; considere estados, tempo, percepções e ações.
*   **Conhecimento do funcionamento:**  Conhecido ou desconhecido para o agente.

##### Comparação final
1. O que muda entre jogar tênis contra outra pessoa e praticar contra uma parede?
No jogo contra outra pessoa, o ambiente é **multiagente e competitivo**, exigindo que o agente preveja e reaja às intenções e estratégias ativas do oponente. Contra a parede, o ambiente é de **agente único**, pois a parede é um objeto passivo regido unicamente pelas leis mecânicas da física, sem objetivos concorrentes.

2. Por que comprar livros usados pode exigir decisões com informações incompletas?
Porque aspectos essenciais do ambiente — como o estado real de conservação física do livro (páginas grifadas, rasgos) e a idoneidade do vendedor — são **parcialmente observáveis** e não podem ser verificados com certeza antes do recebimento do produto.

3. Como outros agentes influenciam futebol e leilões?
No futebol, outros agentes geram necessidade de **cooperação em tempo real** com companheiros de equipe e **antecipação competitiva** para evitar desarmos dos adversários. No leilão, a presença de outros agentes concorrentes altera a medida de utilidade, pois cada lance efetuado por um rival força o agente a decidir entre elevar a oferta ou desistir para não ultrapassar seu orçamento limite.

#### Exercício 2.5
Defina cada termo com suas palavras em duas a quatro linhas e apresente um exemplo.

##### Agente
*  Definição: Qualquer entidade capaz de perceber seu ambiente por meio de sensores e atuar sobre esse ambiente utilizando atuadores.
*  Exemplo: Um robô aspirador de pó que percebe a sujeira através de sensores infravermelhos e atua acionando seus motores e o aspirador.

##### Função de agente
*  Definição: Uma descrição matemática abstrata que estabelece o mapeamento entre qualquer sequência histórica completa de percepções e uma ação correspondente.
*  Exemplo: Uma tabela conceitual que associa o histórico de percepções `[[Quadrado A, Sujo], [Aspirar], [Quadrado A, Limpo]]` à ação `Mover Direita`.

##### Programa de agente
*  Definição: A implementação concreta em código executado em uma arquitetura física real, recebendo apenas a percepção do instante atual para devolver uma ação.
*  Exemplo: Um algoritmo em pseudocódigo com instruções `if-else` executado pelo microcontrolador do robô aspirador.

##### Racionalidade
*  Definição: A propriedade de selecionar a ação que maximiza a medida de desempenho esperada, com base na sequência de percepções até o momento e no conhecimento prévio do agente.
*  Exemplo: Um veículo autônomo que desacelera em pista molhada para maximizar a expectativa de segurança e conforto dos passageiros.

##### Autonomia
*  Definição: A capacidade do agente de aprender e se adaptar a partir de suas próprias percepções ao longo do tempo, compensando limitações do conhecimento prévio do projetista.
*  Exemplo: Um sistema de climatização inteligente que aprende as preferências de horário dos usuários para ajustar sozinho a temperatura sem depender de programação fixa.

##### Agente reativo
*  Definição: Agente simples que seleciona suas ações baseando-se exclusivamente na percepção do momento presente, ignorando o histórico e sem manter estado interno.
*  Exemplo: Um robô aspirador simples que executa a regra: "se o quadrado atual estiver sujo, aspire; caso contrário, mova-se para o outro quadrado".

##### Agente baseado em modelo
*  Definição: Agente que mantém um estado interno para rastrear aspectos não observados do mundo, combinando a percepção atual com o histórico e um modelo de como o ambiente evolui.
*  Exemplo: Um carro autônomo que guarda no seu estado interno a posição de um veículo no ponto cego mesmo quando este não é visível na câmera.

##### Agente baseado em objetivos
*  Definição: Agente que combina informações de estado interno com descrições explícitas de objetivos para planejar e escolher sequências de ações que alcancem situações desejadas.
*  Exemplo: Um sistema de navegação GPS que calcula uma sequência de curvas para conduzir o veículo até um endereço de destino informado pelo motorista.

##### Agente baseado em utilidade
*  Definição: Agente que utiliza uma função utilidade interna para quantificar o grau de satisfação de diferentes estados, permitindo escolhas racionais sob incerteza ou objetivos conflitantes.
*  Exemplo: Um aplicativo de transporte que pondera entre o caminho mais rápido e o de menor custo de pedágio para maximizar a utilidade esperada do usuário.

##### Agente com aprendizagem
*  Definição: Agente dividido em elemento de desempenho, crítico, elemento de aprendizado e gerador de problemas, capaz de aperfeiçoar seus componentes internos a partir da experiência.
*  Exemplo: Um programa de xadrez computacional que ajusta os pesos da sua função de avaliação de peças após analisar os resultados de partidas jogadas anteriormente.

#### Síntese com autômatos
Escolha um caso do item 2.4. Apresente três estados internos, três percepções, três ações e duas regras no formato estado atual + percepção → próximo estado e ação. Explique como estados internos representam informação passada e cite uma limitação da simplificação.
Resposta:
* **Caso Escolhido:** Caso 5 — Praticar tênis contra uma parede.
* **3 Estados Internos (\\(Q\\)):**
  1. \\(q_0\\): Aguardando o quique da bola vinda da parede.
  2. \\(q_1\\): Posicionado e preparando o movimento de devolução (*backhand*).
  3. \\(q_2\\): Executando a batida na bola com a raquete.
* **3 Percepções (\\(\Sigma\\)):**
  1. \\(p_1\\): Bola quicando no chão à esquerda do agente.
  2. \\(p_2\\): Bola aproximando-se na distância e altura ideais de golpe.
  3. \\(p_3\\): Bola ultrapassando a área de alcance.
* **3 Ações (\\(A\\)):**
  1. \\(a_1\\): Mover-se para a esquerda e preparar a armação do braço.
  2. \\(a_2\\): Executar o golpe de raquetada para a frente.
  3. \\(a_3\\): Parar a jogada e recolher nova bola.
* **2 Regras de Transição (\\(\delta\\)):**
  1. \\(\delta(q_0, p_1) \rightarrow (q_1, a_1)\\): Estando em \\(q_0\\) e recebendo a percepção \\(p_1\\), o agente transita para o estado de preparação \\(q_1\\) e executa a ação \\(a_1\\).
  2. \\(\delta(q_1, p_2) \rightarrow (q_2, a_2)\\): Estando em \\(q_1\\) e recebendo a percepção \\(p_2\\), o agente transita para o estado de execução \\(q_2\\) e executa a ação \\(a_2\\).

* **Representação da informação passada:** O estado interno armazena a trajetória prévia da bola e a etapa atual do movimento do corpo do agente, garantindo que a raquetada ocorra com synchronia e postura adequadas, algo impossível se o agente considerasse apenas uma imagem estática no instante atual.
* **Limitação da simplificação:** A modelagem por Autômatos Finitos exige discretizar estados, tempo e ações em um conjunto finito e pequeno. No tênis real, as variáveis físicas (velocidade da bola, efeito *spin*, ângulo do braço, força do vento) variam em um espaço contínuo, e a discretização rígida limita drasticamente a precisão motora fina do robô.

#### Entrega e avaliação
Confira: identificação; nove análises no item 2.3; sete casos completos no item 2.4; dez conceitos no item 2.5; síntese; referências. Nome sugerido: NomeSobrenome_Atividade_AgentesInteligentes. Prazo e envio conforme orientação da professora.

| Critério | Atividade avaliativa (1,0 ponto) A2 |
| ------ | ------ |
| Item 2.3 — correção e argumentação | 30% |
| Item 2.4 — PEAS e classificação justificada | 40% |
| Item 2.5 — precisão conceitual e exemplos | 20% |
| Síntese, organização e referências | 10% |

#### Referências
Material-base:
- RUSSELL, Stuart; NORVIG, Peter. Agentes inteligentes. In: RUSSELL, Stuart; NORVIG, Peter. **Inteligência artificial**. 3. ed. Rio de Janeiro: Elsevier, 2013. cap. 2. p. 33-63.
