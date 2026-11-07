# Premiere — ferramentas da Noé VFX

Duas ferramentas para o **Adobe Premiere Pro**, para Windows e macOS.

## O que tem aqui

| Ferramenta | Para que serve | Versão | Baixar |
| :--- | :--- | :--- | :--- |
| **Premiere Toolkit** | Painel que limpa e organiza o projeto: consolida duplicados e remove tracks vazias da timeline | 1.0.0 | [Windows](release/Premiere%20Toolkit/v1.0.0/Premiere%20Toolkit%201.0.0%20%28Windows%29.zip) · [Mac](release/Premiere%20Toolkit/v1.0.0/Premiere%20Toolkit%201.0.0%20%28Mac%29.zip) |
| **Premiere MCP Bridge** | Deixa assistentes de IA (Claude, Codex) controlarem a timeline e o projeto do Premiere | 1.0.0 | [zip](release/Premiere%20MCP/v1.0.0/Premiere_MCP_1.0.0.zip) |

## Como instalar o Premiere Toolkit

1. Baixe o zip do seu sistema e extraia.
2. Rode o instalador da pasta `Premiere Toolkit` (Windows: `Install_Premiere_Toolkit.bat`). Para remover: `Uninstall_Premiere_Toolkit.bat`.
3. Reinicie o Premiere Pro e abra o painel em **Janela → Extensões**.

O `LEIA-ME.txt` dentro do zip traz o passo a passo completo.

## Como instalar o Premiere MCP Bridge

1. Baixe o zip, extraia e leia o `LEIA-ME.txt`.
2. Rode o instalador do seu sistema (pastas `PC` e `MAC`).
3. Abra o painel da ponte dentro do Premiere. **Ele precisa ficar aberto** para a IA conseguir agir.

Requer o [Node.js](https://nodejs.org) instalado.

### Como funciona

```
Assistente de IA ─▶ servidor MCP (Node.js) ─▶ painel CEP dentro do Premiere ─▶ ExtendScript
```

## Estrutura do repositório

```text
Premiere/
├─ Premiere Toolkit/            painel UXP (código, instaladores, testes e empacotamento)
├─ mcp/                         ponte de IA: servidor Node.js, painel CEP e scripts de instalação
├─ release/<Ferramenta>/vX.Y.Z/ pacote de cada versão (ordem crescente, nada é sobrescrito)
├─ CHANGELOG.md                 histórico de versões
└─ HANDOFF.md  VERSIONING.md    como continuar o projeto e regra de versões
```

## Versões

Versionamento `MAJOR.MINOR.PATCH`. Histórico no [CHANGELOG](CHANGELOG.md); regra em [VERSIONING.md](VERSIONING.md).

## Contato

Noé VFX — [noevfx.com](https://noevfx.com) · [labs@noevfx.com](mailto:labs@noevfx.com)

Adobe e Premiere Pro são marcas da Adobe. Estas ferramentas são independentes e não são afiliadas nem endossadas pela Adobe.
