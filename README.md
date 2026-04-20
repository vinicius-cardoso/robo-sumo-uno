# Robo Sumo Uno

Repositorio do projeto completo do robo sumo: PCB, firmware Arduino, mecanica,
arquivos de fabricacao, BOM, fotos e documentacao.

## Estrutura

```text
.
├── bom/                         # Lista de materiais e fornecedores
├── docs/                        # Requisitos, decisoes e anotacoes do projeto
├── electronics/                 # KiCad, bibliotecas, datasheets e fabricacao da PCB
├── firmware/                    # Sketches Arduino, bibliotecas locais e testes
├── manufacturing/               # Instrucoes finais para fabricar/montar cada parte
├── mechanical/                  # CAD mecanico, desenhos e exports para fabricacao
├── media/                       # Fotos, renders e videos do projeto
├── tests/                       # Logs e evidencias de teste
└── tools/                       # Scripts auxiliares
```

## Regras praticas

- Mantenha arquivos editaveis como fonte da verdade: `.kicad_pro`,
  `.kicad_sch`, `.kicad_pcb`, arquivos CAD nativos e `.ino`.
- Coloque arquivos gerados para fabricacao nas pastas `exports/`,
  `manufacturing/` ou `electronics/manufacturing/`.
- Evite versionar backups, builds temporarios, logs grandes e caches de
  ferramentas.
- Para arquivos grandes e binarios que mudam muito, como videos, renders
  pesados e CADs grandes, considere usar Git LFS.
- Prefira nomes curtos, descritivos e sem espacos, por exemplo
  `base_chassis_v01.step`.

## Fluxo sugerido

1. Registre requisitos e restricoes em `docs/requirements.md`.
2. Desenhe a eletronica em `electronics/kicad/`.
3. Desenvolva o firmware em `firmware/arduino/robo_sumo_uno/`.
4. Modele as pecas em `mechanical/cad/`.
5. Exporte arquivos de fabricacao para `mechanical/exports/` e
   `electronics/manufacturing/`.
6. Atualize `bom/bom.csv` sempre que escolher ou trocar um componente.
7. Use `manufacturing/` para guardar instrucoes enviadas a fabricantes ou usadas
   na montagem.

## Commits

Use commits pequenos e com uma intencao clara, por exemplo:

- `docs: add robot weight requirements`
- `electronics: route motor driver board`
- `firmware: add line sensor calibration`
- `mechanical: update acrylic side plates`

