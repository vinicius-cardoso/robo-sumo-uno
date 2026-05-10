# KiCad Libraries

Copias locais das bibliotecas customizadas usadas pelo projeto.

Essas bibliotecas tambem existem no KiCad global desta maquina, mas foram
copiadas para o repositorio para que a PCB abra corretamente em outra maquina.

- `symbols/robo_sumo_uno_library.kicad_sym`
- `footprints/robo_sumo_uno_library.pretty/`

O projeto KiCad em `../kicad/` referencia estas copias por meio de
`sym-lib-table` e `fp-lib-table` locais.

O modulo buck em `../kicad/modules/buck_converter_5v/` tambem referencia esta
mesma biblioteca local para abrir de forma isolada.
