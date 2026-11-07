# Registro da migração para Codex

## Origem conferida

- Fork analisado: https://github.com/evslanca/fluxo-de-edicao
- Projeto original: https://github.com/LeiteZ/fluxo-de-edicao
- Branch de origem: main
- Tree SHA observado nos dois repositórios: 703561d07d78ab4cf69623b09198273d4e830b9b
- Revisão atual: o commit mais recente ainda é 703561d07d78ab4cf69623b09198273d4e830b9b nos dois repositórios; o SKILL.md de ambos continua idêntico.
- Inventário: 22 arquivos de texto, com skill principal, 13 guias, 6 modelos, README e licença.
- A árvore do fork correspondia à árvore do projeto original no instante desta leitura.

## Por que não rodei desassemblador

O conteúdo de origem é Markdown e não inclui executável, pacote de aplicação, JavaScript executável ou runtime para análise reversa. A orientação do REA usada nesta tarefa direciona repositórios-fonte comuns para inspeção de conteúdo e reserva suas ferramentas de análise para artefatos e runtime adequados. Portanto, a migração foi baseada no texto-fonte completo; não declarei análise dinâmica nem desassemblagem.

## Mapeamento para Codex

| Claude Code | Codex |
|---|---|
| Skill principal como SKILL.md na raiz | Skill de projeto em .agents/skills/fluxo-de-edicao/SKILL.md |
| Invocação /nome-da-skill | Invocação $nome-da-skill |
| Instalação global em ~/.claude/skills | Escopo global em ~/.agents/skills |
| Instalação por projeto em formato específico do Claude | Escopo do projeto em .agents/skills |
| Pasta interna _CLAUDE | Pasta neutra _EDICAO para novos projetos; estados legados são consultados no local, sem mover ou renomear |
| /clear após cada etapa | Continuidade pelo arquivo de estado; nova conversa opcional |
| Descrições específicas do Claude | Instruções de etapa compatíveis com Skills do Codex |

## Comportamento preservado

O processo de ambiente, entrevista, análise de referências, plano de oito etapas, perfil pessoal, regras comuns, escrita gradual de skills, geração tardia de scripts, teste com clipe curto, checkpoint e aprovação do usuário foram mantidos. Os guias e modelos de origem foram incluídos sob references/.

O checkpoint `montagem.md` registra a criação do fluxo pessoal. O estado `_EDICAO/projeto.json` pertence a cada vídeo e não substitui esse checkpoint. A skill mestra gerada aceita projetos antigos com `_CLAUDE/projeto.json`, consultando esse arquivo no local sem renomeá-lo.

## Publicação

- Em 2026-11-07, o usuário autorizou publicar esta migração no fork público indicado.
- Os 24 arquivos do pacote foram adicionados sob `codex/` na branch `main`, commit `9685c22bbf029109c2975085ba6c5dc7b19b5d70`.
- A comparação com o commit anterior registra 24 arquivos adicionados e nenhum arquivo original alterado ou removido.
- O repositório continua público; nenhum ajuste de visibilidade foi feito.
