# Buck Converter 5V

Modulo KiCad importado do projeto:

`~/projects/pcb/buck-converter/buck-converter-v2`

Arquivos principais:

- `buck_converter_5v.kicad_sch`: esquematico do buck de 5 V.
- `buck_converter_5v.kicad_pcb`: layout roteado do buck de 5 V.
- `buck_converter_5v.kicad_pro`: projeto KiCad auxiliar para abrir o modulo isoladamente.

Os simbolos e footprints customizados foram ajustados para usar a biblioteca local
do projeto, com o nickname `robo_sumo_uno_library`.

Bibliotecas customizadas usadas pelo modulo:

- simbolos: `LMR14050`, `KF301-2P`;
- footprints: `HANDSON_KF301-2P`, `Inductor B82477P4682M000`, `TO-277A`.

Todos esses itens ficam em `electronics/libraries/`.

## Validacao apos importacao

- PCB isolada: DRC com 0 violacoes e 0 itens desconectados.
- Esquematico isolado: ERC herdou 3 erros de power pin sem driver e 0 avisos.

Os erros de power pin devem ser resolvidos com `PWR_FLAG` ou pela integracao com
as fontes reais no esquematico principal.

## Como usar no projeto principal

1. Abra o projeto principal em `electronics/kicad/robo-sumo.kicad_pro`.
2. No editor de esquematico, importe ou copie o circuito de
   `modules/buck_converter_5v/buck_converter_5v.kicad_sch`.
3. Reanote as referencias se houver conflito com componentes existentes.
4. Faca as conexoes de entrada, saida e GND aos nets do robo.
5. No editor da PCB, use o layout de
   `modules/buck_converter_5v/buck_converter_5v.kicad_pcb` como referencia ou
   append/copy do bloco fisico.
6. Depois de integrar, rode ERC e DRC no projeto principal.

Para dois bucks, duplique o bloco somente depois de reanotar as referencias e
confirmar os nomes dos nets de entrada/saida.
