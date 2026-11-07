<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=9b59b6&height=220&section=header&text=NOVA&fontColor=ffffff&fontSize=72&fontAlignY=38&desc=Product%20Owner&descSize=22&descAlignY=60" width="100%" />

<img src="./assets/portrait.png" width="200" alt="Nova" />

# 🎯 Nova · Product Owner

**Transforma intencao de negocio em especificacao executavel: desenho da solucao, criterios verificaveis e prioridade justificada por valor.**

![Skills](https://img.shields.io/badge/skills-5-9b59b6?style=for-the-badge)
![CLIs](https://img.shields.io/badge/CLIs-8-2980b9?style=for-the-badge)
![Idioma](https://img.shields.io/badge/pt--BR-nativo-1abc9c?style=for-the-badge)

</div>

---

## Por que usar este agente

- **Elimina retrabalho por ambiguidade.** O desenho previo resolve no texto o que custaria duas rodadas de implementacao.
- **Criterio de aceite testavel.** Quem implementa sabe quando parou; quem valida sabe o que medir.
- **Prioridade defensavel.** Cada item da fila tem valor, custo e justificativa escritos.
- **Casos de erro desde o inicio.** Entrada vazia, duplicada, no limite e falha de rede entram na especificacao, nao na correcao emergencial.
- **Rastro de decisao.** Seis meses depois da-se para saber por que a escolha foi aquela.

---

## Skills

| Skill | Titulo | O que resolve |
|---|---|---|
| [`desenho-de-atividade`](skills/desenho-de-atividade/SKILL.md) | Desenho de atividade (blueprint) | Produzir o documento que antecede a implementacao: objetivo, decisoes tecnicas, arquivos afetados, checklist e casos de uso. |
| [`historias-de-usuario`](skills/historias-de-usuario/SKILL.md) | Historias de usuario e refinamento | Escrever historias no formato persona-acao-beneficio, quebrar epicos e definir a condicao de pronto compartilhada. |
| [`priorizacao`](skills/priorizacao/SKILL.md) | Priorizacao de fila | Ordenar a fila por valor e custo com justificativa escrita, usando classificacao de obrigatoriedade e matriz impacto/esforco. |
| [`metricas-de-produto`](skills/metricas-de-produto/SKILL.md) | Metricas de produto | Definir e acompanhar metricas de aquisicao, ativacao, retencao, receita e indicacao, ligando cada entrega a um indicador. |
| [`comunicacao-de-status`](skills/comunicacao-de-status/SKILL.md) | Comunicacao de status e decisao | Reportar andamento, bloqueio e decisao de forma objetiva, com fidelidade ao que realmente aconteceu. |

Cada skill e um arquivo markdown autocontido (`skills/<slug>/SKILL.md`): pode ser instalada
isolada, sem o resto do repositorio.

---

## Instalacao rapida

```bash
git clone https://github.com/WallysonDuarte/agente-nova.git
cd agente-nova

# Claude Code — skills nativas
cp -r skills/* ~/.claude/skills/

# Qualquer outra CLI — arquivo unico de instrucao
cat AGENT.md skills/*/SKILL.md > AGENTS.md
```

| CLI | Instalacao (Windows / PowerShell) | Onde colocar as skills | Rodar |
|---|---|---|---|
| **Claude Code** | `irm https://claude.ai/install.ps1 | iex` | `~/.claude/skills/` | `claude -p "<pedido>"` |
| **Codex** | `irm https://chatgpt.com/codex/install.ps1 | iex` | `AGENTS.md na raiz do projeto` | `codex exec --skip-git-repo-check "<pedido>"` |
| **Grok** | `irm https://x.ai/cli/install.ps1 | iex` | `passado no prompt` | `grok -p "<pedido>"` |
| **Antigravity** | `irm https://antigravity.google/cli/install.ps1 | iex` | `passado no prompt` | `agy -p "<pedido>"` |
| **Hermes** | `iex (irm https://hermes-agent.nousresearch.com/install.ps1)` | `passado no prompt` | `hermes` |
| **OpenClaw** | `& ([scriptblock]::Create((iwr -useb https://openclaw.ai/install.ps1))) -NoOnboard` | `~/.openclaw/skills/` | `openclaw agent --local -m "<pedido>"` |
| **OpenCode** | `irm https://opencode.ai/install | iex` | `AGENTS.md na raiz do projeto` | `opencode` |
| **Kimi Code** | `irm https://code.kimi.com/kimi-code/install.ps1 | iex` | `passado no prompt` | `kimi -p "<pedido>"` |

Passo a passo por CLI, incluindo macOS/Linux: **[install/README.md](install/README.md)**

---

## Estrutura

```
agente-nova/
├── AGENT.md                 definicao canonica do agente
├── .agent/agent.json        metadados legiveis por maquina
├── skills/
│   └── desenho-de-atividade/SKILL.md
│   └── historias-de-usuario/SKILL.md
│   └── priorizacao/SKILL.md
│   └── metricas-de-produto/SKILL.md
│   └── comunicacao-de-status/SKILL.md
├── install/README.md        instalacao nas 8 CLIs
└── assets/portrait.png
```

---

## Ecossistema

Este agente faz parte de um time de 9 agentes especializados:

[![Master](https://img.shields.io/badge/Master-00ff41?style=flat-square)](https://github.com/WallysonDuarte/agente-master) [![Nova](https://img.shields.io/badge/Nova-9b59b6?style=flat-square)](https://github.com/WallysonDuarte/agente-nova) [![Atlas](https://img.shields.io/badge/Atlas-1abc9c?style=flat-square)](https://github.com/WallysonDuarte/agente-atlas) [![Pixel](https://img.shields.io/badge/Pixel-e91e63?style=flat-square)](https://github.com/WallysonDuarte/agente-pixel) [![Forge](https://img.shields.io/badge/Forge-e67e22?style=flat-square)](https://github.com/WallysonDuarte/agente-forge) [![Cipher](https://img.shields.io/badge/Cipher-c0392b?style=flat-square)](https://github.com/WallysonDuarte/agente-cipher) [![Luna](https://img.shields.io/badge/Luna-f39c12?style=flat-square)](https://github.com/WallysonDuarte/agente-luna) [![Lira](https://img.shields.io/badge/Lira-f0932b?style=flat-square)](https://github.com/WallysonDuarte/agente-lira) [![Rank](https://img.shields.io/badge/Rank-2980b9?style=flat-square)](https://github.com/WallysonDuarte/agente-rank)

[![Hub](https://img.shields.io/badge/ver%20o%20time%20completo-9b59b6?style=for-the-badge)](https://github.com/WallysonDuarte/softwarehub-agentes)

---

<div align="center">

## Apoie este trabalho

Os 9 agentes sao mantidos de forma independente e publicados abertamente.
Se este material te poupou tempo, voce pode retribuir com um cafe:

<a href="https://buy.stripe.com/bJefZi3wJ4JH18WeuEgA800">
<img src="https://img.shields.io/badge/Apoie--me-R$%2010-9b59b6?style=for-the-badge&logo=stripe&logoColor=white" alt="Apoie-me com R$ 10" />
</a>

## Links

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dududev/)
[![Do Zero ao Junior](https://img.shields.io/badge/Do%20Zero%20ao%20Junior-1abc9c?style=for-the-badge)](https://dozeroaojunior.com.br/)
[![Curitiba Software](https://img.shields.io/badge/Curitiba%20Software-2980b9?style=for-the-badge)](https://curitibasoftware.com.br/)
[![SoftwareHub](https://img.shields.io/badge/SoftwareHub-00ff41?style=for-the-badge)](https://softwarehub.com.br/)


</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=9b59b6&height=100&section=footer" width="100%" />
