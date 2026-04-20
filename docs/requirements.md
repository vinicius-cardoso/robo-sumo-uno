# Requisitos

Fonte principal: [Regulamento Sumo 2025](regulations/sumo_2025_regulamento.pdf),
12a CoRA, categoria Robo Sumo.

Categoria deste projeto: Robo Sumo de 1 kg.

## Resumo de Competicao

- Competicao: 12a Competicao de Robos Autonomos (CoRA), UFMG, 2025.
- Categoria: Robo Sumo.
- Peso maximo oficial: 1 kg.
- Dimensoes maximas oficiais antes do inicio do round: 15,2 cm x 15,2 cm.
- Altura: sem limite oficial.
- Alimentacao: exclusivamente eletrica e embarcada no robo.
- Tensao de alimentacao: sem limite oficial no regulamento.
- Controle: autonomo, sem comunicacao externa.

## Requisitos Obrigatorios do Robo

| ID | Requisito | Origem |
| --- | --- | --- |
| REQ-RS-001 | O robo deve ser autonomo durante a partida. | Regulamento 2.2.1 |
| REQ-RS-002 | O robo nao pode usar comunicacao externa durante a partida. | Regulamento 2.2.1 |
| REQ-RS-003 | Qualquer radio do controlador, como Wi-Fi ou Bluetooth, deve ficar desabilitado ou sem uso competitivo durante o round. | Derivado de REQ-RS-002 |
| REQ-RS-004 | O robo deve ser movido exclusivamente por energia eletrica. | Regulamento 2.2.2 |
| REQ-RS-005 | Toda fonte de alimentacao deve estar embarcada no robo. | Regulamento 2.2.2 |
| REQ-RS-006 | O robo nao pode depender de fonte externa, cabo, carregador ou alimentacao fora do robo durante o round. | Regulamento 2.2.2 |
| REQ-RS-007 | A massa total em condicao de disputa deve ser menor ou igual a 1000 g. | Regulamento 2.2.4 |
| REQ-RS-008 | O robo deve caber em 152 mm x 152 mm antes do anuncio de inicio do round. | Regulamento 2.2.5 |
| REQ-RS-009 | A altura do robo pode ser livre, desde que os demais requisitos sejam atendidos. | Regulamento 2.2.5 |
| REQ-RS-010 | O robo pode expandir depois do inicio da partida, desde que continue fisicamente como um unico robo. | Regulamento 2.2 |
| REQ-RS-011 | Partes estruturais ou funcionais nao podem se separar do robo durante a partida. | Regulamento 2.2 |
| REQ-RS-012 | Parafusos e porcas soltos sao tratados como excecao pelo regulamento, mas o projeto deve evitar qualquer desprendimento. | Regulamento 2.2 |
| REQ-RS-013 | Nao usar Lego no robo. | Regulamento 2.2.6 |
| REQ-RS-014 | O robo nao pode ter pecas que danifiquem ou quebrem o ringue. | Regulamento 2.2.7 |
| REQ-RS-015 | Arestas externas nao podem ser afiadas a ponto de danificar ou arranhar o ringue. | Regulamento 2.2.8 |
| REQ-RS-016 | O robo nao pode ter dispositivos projetados para danificar intencionalmente o oponente. | Regulamento 2.2.9 |
| REQ-RS-017 | Nao usar dispositivos ou materiais inflamaveis. | Regulamento 2.2.10 |
| REQ-RS-018 | Nao usar reservatorios ou mecanismos para lancar liquido, po, gas ou substancias no oponente. | Regulamento 2.2.11 |
| REQ-RS-019 | Nao usar pecas ou componentes cortantes. | Regulamento 2.2.12 |
| REQ-RS-020 | Nao usar dispositivos de interferencia contra o oponente. | Regulamento 2.2.13 |
| REQ-RS-021 | Nao usar LEDs IR ou sistemas equivalentes com a intencao de saturar sensores do oponente. | Regulamento 2.2.13 |
| REQ-RS-022 | Nao usar dispositivos que aumentem a forca normal interagindo diretamente com a superficie, como vacuo ou imas. | Regulamento 2.2.14 |
| REQ-RS-023 | Nao usar dispositivos que melhorem a tracao por interacao direta com a superficie. | Regulamento 2.2.15 |

## Requisitos de Firmware

| ID | Requisito | Origem |
| --- | --- | --- |
| REQ-FW-001 | O firmware deve iniciar o comportamento autonomo somente depois de 5 s da ativacao pelo representante da equipe. | Regulamento 2.4 |
| REQ-FW-002 | Durante os 5 s iniciais, o robo deve permanecer parado. | Regulamento 2.4 |
| REQ-FW-003 | O firmware deve operar sem comandos externos apos a ativacao. | Regulamento 2.2.1 e 2.4 |
| REQ-FW-004 | O firmware deve considerar round maximo de 1 min 30 s como tempo de referencia de autonomia e estrategia. | Regulamento 2.5 |
| REQ-FW-005 | O controle deve tolerar reinicio de round quando os robos ficarem presos ou orbitando sem progresso. | Regulamento 2.4 |
| REQ-FW-006 | Sensores de borda devem ser calibraveis, pois o dojo de teste pode ter tonalidade diferente do dojo oficial. | Regulamento 2.3.1 |

## Requisitos de Mecanica

| ID | Requisito | Origem |
| --- | --- | --- |
| REQ-MEC-001 | O envelope mecanico inicial deve ficar dentro de 152 mm x 152 mm. | Regulamento 2.2.5 |
| REQ-MEC-002 | A massa mecanica, somada a eletronica, bateria e fixadores, deve ficar abaixo de 1000 g. | Regulamento 2.2.4 |
| REQ-MEC-003 | Bordas, rampas e pa frontal devem ter acabamento que nao risque nem danifique o ringue. | Regulamento 2.2.7 e 2.2.8 |
| REQ-MEC-004 | Qualquer mecanismo expansivel deve permanecer preso ao robo durante todo o round. | Regulamento 2.2 |
| REQ-MEC-005 | Componentes devem ser fixados para resistir a impacto sem se desprender. | Regulamento 2.2 |
| REQ-MEC-006 | Materiais inflamaveis devem ser evitados na estrutura e em qualquer mecanismo exposto. | Regulamento 2.2.10 |
| REQ-MEC-007 | Nao projetar armas, laminas, pontas cortantes ou sistemas com funcao principal de danificar o oponente. | Regulamento 2.2.9 e 2.2.12 |
| REQ-MEC-008 | Nao usar imas, bombas de vacuo, adesivos ativos ou sistemas similares que interajam diretamente com a superficie para aumentar normal ou tracao. | Regulamento 2.2.14 e 2.2.15 |

## Requisitos de Eletronica

| ID | Requisito | Origem |
| --- | --- | --- |
| REQ-ELE-001 | A bateria deve ser embarcada e capaz de alimentar todo o sistema sem cabo externo durante a partida. | Regulamento 2.2.2 |
| REQ-ELE-002 | A arquitetura eletrica pode usar a tensao necessaria ao projeto, pois nao ha limite oficial de tensao no regulamento. | Regulamento 2.2.3 |
| REQ-ELE-003 | O projeto deve incluir protecao e fixacao adequadas para bateria e cabos, evitando desconexao por impacto. | Derivado de REQ-RS-005 e REQ-MEC-005 |
| REQ-ELE-004 | Emissores IR usados para sensoriamento proprio nao podem ser projetados para interferir nos sensores adversarios. | Regulamento 2.2.13 |

## Arena e Condicoes de Projeto

- Superficie do dojo oficial: madeira.
- Diametro do dojo: 770 mm.
- Espessura do dojo: 25 mm.
- Linhas Shikiri: 10 mm de largura e 100 mm de comprimento.
- Distancia entre linhas Shikiri: 100 mm.
- O robo deve iniciar atras da linha Shikiri ou de uma linha imaginaria colinear a ela.
- O robo nao pode ter parte posicionada alem da borda interna da linha Shikiri no inicio.
- O dojo de teste pode ter cores ou tonalidades diferentes do dojo oficial.

## Regras Operacionais que Afetam o Projeto

- Apenas o capitao posiciona o robo no dojo.
- Depois do comando do juiz, o representante ativa o robo e se afasta.
- O robo deve aguardar 5 s antes de se mover.
- Cada round dura no maximo 1 min 30 s.
- Nao sao permitidas alteracoes no robo entre rounds de uma mesma partida.
- Alteracoes podem ser feitas entre partidas, desde que a equipe ainda nao tenha sido convocada para a area do confronto.
- Se o robo perder uma peca que prejudique o adversario, o adversario pode ser considerado vencedor.

## Alvos Internos de Projeto

Estes limites nao sao regras oficiais, mas reduzem risco de reprovacao na medicao:

- Massa alvo: no maximo 950 g, deixando margem para parafusos, cabos e pequenas alteracoes.
- Envelope alvo: no maximo 150 mm x 150 mm antes do inicio do round.
- Autonomia alvo: pelo menos 5 min de operacao agressiva, acima do tempo maximo de um round.
- Firmware: manter Wi-Fi e Bluetooth explicitamente desabilitados durante o modo de competicao.
- Sensores de linha: permitir calibracao rapida antes da partida.
- Estrutura: revisar todas as bordas tocaveis antes da homologacao.

## Checklist de Homologacao

- [ ] Massa total medida menor ou igual a 1000 g.
- [ ] Robo cabe em 152 mm x 152 mm antes do round.
- [ ] Robo permanece parado por 5 s apos ativacao.
- [ ] Sem comunicacao externa no modo de competicao.
- [ ] Alimentacao totalmente embarcada.
- [ ] Sem cabos externos durante o round.
- [ ] Sem Lego.
- [ ] Sem pecas cortantes.
- [ ] Sem arestas capazes de riscar o ringue.
- [ ] Sem material ou dispositivo inflamavel.
- [ ] Sem mecanismo para lancar liquido, po, gas ou substancias.
- [ ] Sem sistema de interferencia contra sensores adversarios.
- [ ] Sem ima, vacuo ou sistema ativo de aumento de normal.
- [ ] Sem sistema de tracao que interaja diretamente com a superficie.
- [ ] Componentes bem fixados contra impacto.
- [ ] Sensores calibrados para a tonalidade do dojo disponivel.
