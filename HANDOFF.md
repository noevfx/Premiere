# Premiere — HANDOFF

Raiz do repositório `noevfx/Premiere` (git próprio). Dois produtos: **Premiere Toolkit** (painel UXP) e **Premiere MCP** (ponte para agentes de IA). Regras gerais: `D:\.IA agents\global\AGENTS.md`, `PR_PATTERNS.md` e `RELEASES.md`.

## Mapa

```text
Premiere\
├─ Premiere Toolkit\   plugin\ (painel UXP), install\ (Windows/Mac), test\, tools\pack.mjs
├─ mcp\                server\ (Node.js, premiere-bridge), cep-panel\, skill\, PC\ e MAC\ (instaladores), build_zip.py
├─ release\<Produto>\vX.Y.Z\   pacotes de cada versão, em ordem crescente
├─ CHANGELOG.md  HANDOFF.md  README.md  VERSIONING.md  AGENTS.md  CLAUDE.md
```

## Build e empacotamento

- Toolkit: `node "Premiere Toolkit/tools/pack.mjs"` → `release/Premiere Toolkit/v<manifest>/` (zips Windows e Mac). A versão vem de `plugin/manifest.json`.
- MCP: `python mcp/build_zip.py` → `release/Premiere MCP/v<package.json>/Premiere_MCP_<versão>.zip`. A versão vem de `mcp/server/package.json`.
- **Nunca rodar o empacotador de uma versão já publicada**: os zips carregam data/hora e mudam de conteúdo; correção vira nova versão.

## Instalação para teste

- Toolkit: `Premiere Toolkit/install/Install_Premiere_Toolkit.bat` (ou `.command` no Mac).
- MCP: servidor instalado em `%APPDATA%\prmcp\server\index.js` (é o que o Claude Code usa, server `premiere-bridge`) e painel em `%APPDATA%\Adobe\CEP\extensions\com.prmcp.bridge`. A cópia instalada é independente da fonte: depois de editar a fonte, reinstalar.

## Como lançar uma versão

Seguir `D:\.IA agents\global\RELEASES.md`: backup em `_backups\` → bump (manifest.json / package.json) e `CHANGELOG.md` → empacotar → commit → publicar e espelhar no Drive. Atualizar também a tag (`premiere-toolkit-vX.Y.Z`, `premiere-mcp-vX.Y.Z`).

## Estado (2026-10-25)

- Reorganizado em 2026-10-25 (ver `CHANGELOG.md`). Ainda nada foi enviado ao GitHub: os repositórios `noevfx/...` serão criados e enviados só com ordem do Eduardo ("pode subir pro git").
- Armadilhas de scripting do Premiere (cores em int64, ordem do `addVideoEffect`, índice do QE, salvar trava) estão em `PR_PATTERNS.md` e na memória do agente.
