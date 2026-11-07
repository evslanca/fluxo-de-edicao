# Fluxo de edição — Codex

Pacote de skill para montar um fluxo de edição de vídeo pessoal, etapa por etapa. A skill não edita o vídeo: ela ajuda a pessoa a definir o processo e criar skills próprias para cortes, motion, câmera, som e as demais etapas necessárias.

## Instalar

Abra esta pasta como projeto no Codex. A skill do projeto está em:

`.agents/skills/fluxo-de-edicao/`

Para disponibilizá-la em todos os projetos, copie somente a pasta `fluxo-de-edicao` para `~/.agents/skills/`. A documentação do Codex também reconhece skills locais de projeto em `.agents/skills/`.

## Usar

No Codex, invoque:

`$fluxo-de-edicao`

Para continuar uma montagem existente, informe a pasta de ferramentas onde está `montagem.md`. A skill mostra o checkpoint antes de retomar.

Há dois estados diferentes: `montagem.md` registra a criação do seu fluxo pessoal; `_EDICAO/projeto.json` registra o progresso de cada vídeo. A skill mestra gerada também reconhece o estado antigo em `_CLAUDE/projeto.json` e o consulta no local, sem movê-lo.

No Windows, a instalação para todos os projetos fica em `%USERPROFILE%\.agents\skills\fluxo-de-edicao`. Depois de copiar a pasta, inicie uma nova sessão do Codex para carregar a skill.

## O que foi preservado

- O fluxo inicial de oito etapas e as adaptações para Reels, vídeo sem motion e trabalho sem editor de vídeo.
- Os guias de decisões, referências, motion, HyperFrames, entrega para o editor e princípios técnicos.
- Os modelos da montagem, perfil, estado do vídeo, regras comuns, skill mestra e skills por etapa.
- As proteções contra sobrescrever skills, apagar ou mover arquivos originais e instalar ferramentas sem autorização.

## Licença e origem

A migração deriva da skill MIT de Lucas Leite. O conteúdo de referência está em [LeiteZ/fluxo-de-edicao](https://github.com/LeiteZ/fluxo-de-edicao); o fork do usuário apontava para o mesmo tree SHA no momento da leitura. Veja `MIGRACAO-CODEX.md` para o mapeamento e o registro da origem. A licença original acompanha este pacote.

## Documentação do Codex

- [Skills no Codex](https://developers.openai.com/plugins/concepts/skills)
- [Criar skills](https://developers.openai.com/plugins/build/skills)
