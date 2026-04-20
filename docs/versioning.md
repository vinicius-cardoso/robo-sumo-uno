# Versionamento

Este projeto usa Git para controlar as versoes dos arquivos de eletronica,
firmware, mecanica, fabricacao e documentacao.

Como o projeto sera mantido por uma pessoa, o fluxo recomendado e simples:

- manter a branch `main` como historico principal do projeto;
- fazer commits pequenos, cada um com uma intencao clara;
- usar tags para marcar versoes importantes da PCB, firmware ou mecanica;
- criar branches apenas para testar alternativas maiores.

## Fluxo diario

Depois de alterar arquivos do projeto:

```bash
git status
git add caminho/do/arquivo
git commit -m "tipo: descricao curta da mudanca"
git push
```

Exemplos de commits:

```bash
git commit -m "pcb: position main components"
git commit -m "pcb: route power tracks"
git commit -m "firmware: add line sensor calibration"
git commit -m "mechanical: update acrylic side plates"
git commit -m "docs: add assembly notes"
```

## Tags para marcos

Use tags quando quiser congelar um ponto importante do projeto e voltar nele
facilmente depois.

Exemplo: marcar a versao da PCB com componentes posicionados, mas sem trilhas
roteadas:

```bash
git tag -a pcb-v0.1-unrouted -m "PCB com componentes posicionados e trilhas ainda nao roteadas"
git push origin pcb-v0.1-unrouted
```

Exemplo: marcar a versao com as trilhas de power roteadas:

```bash
git tag -a pcb-v0.2-power-routed -m "PCB com trilhas de power roteadas"
git push origin pcb-v0.2-power-routed
```

Sugestao de marcos para a PCB:

- `pcb-v0.1-unrouted`: componentes posicionados e trilhas ainda nao roteadas;
- `pcb-v0.2-power-routed`: trilhas de alimentacao roteadas;
- `pcb-v0.3-motor-routing`: etapa de roteamento dos drivers/motores;
- `pcb-v0.4-signal-routing`: sinais principais roteados;
- `pcb-v0.5-drc-clean`: DRC revisado e sem erros relevantes;
- `pcb-v1.0-fabrication-ready`: versao pronta para gerar arquivos de fabricacao.

Tambem e possivel usar tags para firmware e mecanica:

- `firmware-v0.1-sensor-readout`
- `firmware-v0.2-motor-control`
- `mechanical-v0.1-layout`
- `mechanical-v1.0-fabrication-ready`

## Voltando para uma versao antiga

Para consultar uma tag sem alterar a `main`:

```bash
git switch --detach pcb-v0.2-power-routed
```

Para criar uma branch nova a partir de uma tag e experimentar mudancas:

```bash
git switch -c revisar-power pcb-v0.2-power-routed
```

Quando terminar de consultar uma versao antiga, volte para a `main`:

```bash
git switch main
```

## Quando usar branches

Use branches quando a mudanca for experimental ou puder demorar varios commits.

Exemplos:

```bash
git switch -c experimento-layout-pcb
git switch -c firmware-novo-controle-motores
git switch -c mecanica-base-aco-v2
```

Depois, se a ideia funcionar, integre na `main`:

```bash
git switch main
git merge experimento-layout-pcb
git push
```

Se a ideia nao for usada, a branch pode ficar guardada como referencia ou ser
apagada depois.

## Releases no GitHub

Para versoes enviadas para fabricacao, crie tambem uma Release no GitHub.

Uma Release de PCB deve anexar, quando existirem:

- Gerbers;
- arquivos de furo/drill;
- BOM;
- PDF do esquematico;
- PDF ou imagem da PCB;
- anotacoes de fabricacao.

Isso deixa claro exatamente qual versao foi fabricada e facilita repetir ou
corrigir a producao no futuro.
