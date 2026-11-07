# Changelog — Premiere

Versionamento semântico **por produto**. Cada versão fica em `release/<Produto>/vX.Y.Z/` e não é sobrescrita (diretriz: `D:\.IA agents\global\RELEASES.md`). Tags no git: `premiere-toolkit-v1.0.0`, `premiere-mcp-v1.0.0`.

## Versões atuais

| Produto | Versão | Tipo | Pacote |
| :--- | :--- | :--- | :--- |
| Premiere Toolkit | 1.0.0 | painel UXP | `release/Premiere Toolkit/v1.0.0/` (Windows e Mac) |
| Premiere MCP | 1.0.0 | servidor MCP + painel CEP + skill | `release/Premiere MCP/v1.0.0/` |

---

## Repositório

### 2026-10-25 — Reorganização
- Zips que ficavam soltos dentro das pastas dos produtos foram para `release/<Produto>/vX.Y.Z/`.
- `tools/pack.mjs` (Toolkit) e `mcp/build_zip.py` (MCP) agora gravam direto em `release/` e deixam as versões antigas intactas (antes o `build_zip.py` apagava o zip anterior).
- Duas cópias idênticas do projeto (`Premiere-mcp`, com histórico git local próprio, e `Scripts Premiere`, sem git) foram para `_Arquivo\Premiere` em `D:\Noe VFX\.Labs`.

---

## Premiere Toolkit

### [1.0.0] — 2026-10-20
- Painel UXP oficial para o Adobe Premiere Pro: limpeza e organização do projeto, consolidação de duplicados e remoção de tracks vazias na timeline.
- Instaladores para Windows e macOS; pacotes `Premiere Toolkit 1.0.0 (Windows).zip` e `(Mac).zip`.
- Substitui o painel UXP legado (`uxp-panel`, 0.1.1 de 2026-08-15, que nasceu como painel de keyframes com motor procedural em GPU e foi descartado).

## Premiere MCP

### [1.0.0] — 2026-10-20
- Servidor Model Context Protocol (`premiere-bridge`, Node.js) e painel CEP (`com.prmcp.bridge`) para controlar projeto e timeline do Premiere Pro por agentes de IA.
- Instaladores PC e MAC e o pacote `Premiere_MCP_1.0.0.zip` (com skill `premiere-bridge`).
- Unificado neste repositório em 2026-10-20 (antes vivia em um repositório local separado).
