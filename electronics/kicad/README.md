# KiCad

Projeto principal da PCB do robo.

Arquivos que devem ser versionados:

- `robo-sumo.kicad_pro`: projeto KiCad.
- `robo-sumo.kicad_sch`: esquematico.
- `robo-sumo.kicad_pcb`: layout da PCB.
- `sym-lib-table`: bibliotecas de simbolos locais do projeto.
- `fp-lib-table`: bibliotecas de footprints locais do projeto.

As bibliotecas customizadas aparecem no KiCad com o nickname
`robo_sumo_uno_library`.

Arquivos locais/gerados pelo KiCad ficam no mesmo diretorio para o programa
funcionar normalmente, mas sao ignorados pelo Git:

- `robo-sumo.kicad_prl`
- `fp-info-cache`
- `robo-sumo-backups/`
