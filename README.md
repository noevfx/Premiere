# Premiere

Repositorio de scripts, painéis e ferramentas de automação para Adobe Premiere Pro.

## Projetos atuais

- **Premiere Toolkit (v1.0.0)**: Painel UXP oficial para Adobe Premiere Pro. Limpeza e organização de projeto, consolidação de duplicados e remoção de tracks vazias na timeline.
- **Premiere MCP Bridge (v1.0.0)**: Servidor Model Context Protocol (MCP) e extensão CEP para controle e automação remota da timeline e projeto do Premiere Pro via agentes de IA.

## Estrutura do Repositório

```text
Premiere/
  ├── Premiere Toolkit/        # Painel UXP oficial
  │     ├── plugin/
  │     ├── install/
  │     ├── test/
  │     ├── tools/
  │     └── tools/pack.mjs     # gera os zips em release/Premiere Toolkit/vX.Y.Z/
  ├── mcp/                     # Ponte MCP & Automação da Timeline
  │     ├── server/            # Servidor Node.js do premiere-bridge
  │     ├── cep-panel/         # Painel CEP de ponte com o Premiere
  │     ├── skill/             # Skill premiere-bridge para agentes de IA
  │     ├── PC/ & MAC/         # Scripts de instalação
  │     └── build_zip.py       # gera o zip em release/Premiere MCP/vX.Y.Z/
  ├── release/                 # pacotes de cada versão, em ordem crescente
  │     ├── Premiere Toolkit/v1.0.0/
  │     └── Premiere MCP/v1.0.0/
  ├── CHANGELOG.md  HANDOFF.md
  └── README.md
```

## Releases

Cada produto tem a sua pasta de versões em `release/<Produto>/vX.Y.Z/` (ordem crescente, nada é sobrescrito); histórico em [`CHANGELOG.md`](CHANGELOG.md). Os instaladores para Windows e macOS também estão na aba [Releases](https://github.com/noevfx/Premiere/releases).

## Diretrizes de Desenvolvimento

Antes de alterar qualquer script, painel ou arquivo de empacotamento, consulte:

1. `VERSIONING.md`
2. `AGENTS.md`
3. `CLAUDE.md`

Sempre siga o versionamento SemVer (`MAJOR.MINOR.PATCH`) e faça commits em português com prefixos semânticos padronizados.
