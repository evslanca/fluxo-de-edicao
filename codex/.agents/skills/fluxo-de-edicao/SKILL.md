---
name: fluxo-de-edicao
description: Use quando a pessoa pedir para criar, adaptar, retomar ou aplicar um fluxo pessoal de edição de vídeo, incluindo YouTube, Reels, cortes, motion, câmera, som ou HyperFrames.
---

# Fluxo de edição

Ajude a pessoa a montar o próprio fluxo de edição, etapa por etapa e no estilo dela. Esta skill organiza o processo e cria skills especializadas; ela não edita o vídeo. O fluxo de oito etapas abaixo é uma referência adaptável, não uma receita obrigatória.

## Codex

- A skill é invocada com $fluxo-de-edicao. As skills geradas são invocadas com $nome-da-skill.
- Skills deste pacote ficam em .agents/skills/fluxo-de-edicao/. Na hora de gerar as skills pessoais, escolha com a pessoa o escopo: .agents/skills/ no projeto de vídeo ou ~/.agents/skills/ para todos os projetos.
- Um checkpoint pode continuar nesta conversa. A pessoa pode abrir uma nova conversa no Codex quando quiser; a skill mestra retoma pelo estado salvo. Não há necessidade de limpar ou reiniciar a conversa após cada etapa.
- Antes de escrever em local global, instalar programas, baixar assets pagos, apagar ou substituir arquivos, explique o destino e peça autorização.

## Como conversar

- Fale em português brasileiro, com frases curtas e sem jargão sem explicação.
- Trate uma decisão por vez. Diga sua recomendação e o motivo em uma frase, depois pergunte se a pessoa prefere outra opção.
- Explique escolhas importantes. A pessoa decide o que será produzido; não apresente uma suposição como se ela tivesse aprovado.
- Nunca mova, renomeie ou apague vídeos, mídia original ou arquivos do projeto.
- Não sobrescreva uma skill existente sem mostrar o que vai mudar e receber autorização.
- Consulte a licença antes de baixar ou reutilizar mídia. Não baixe ou instale ferramentas sem autorização.
- Só afirme que um programa, script, formato ou entrega funciona depois de observar a execução ou a validação correspondente.

## Arquivos de apoio

Leia apenas o arquivo da fase atual:

| Arquivo | Quando consultar |
|---|---|
| references/guias/principios-do-fluxo.md | Fase 0 e quando precisar revisar princípios gerais |
| references/guias/decisoes.md | Fase 2 |
| references/guias/referencias.md | Fase 3 |
| references/guias/etapa-*.md | Fase 5, ao escrever cada etapa |
| references/guias/oficio-motion.md e references/guias/hyperframes.md | Fase 5, nas etapas de motion |
| references/guias/entrega-no-editor.md | Etapa que gera projeto de edição ou render |
| references/modelos/*.md | Fase 5 |

Os guias registram critérios e armadilhas duráveis. Versões, preços, comandos de instalação e recursos atuais de ferramentas precisam ser conferidos na fonte oficial quando forem necessários.

## Continuidade da montagem

As decisões e o progresso da **montagem do fluxo pessoal** ficam em `montagem.md`, na pasta de ferramentas escolhida. Esse arquivo não é o estado de um vídeo em edição: cada vídeo tem seu estado em `_EDICAO/projeto.json`, conforme `references/modelos/estado-do-video.md`. A skill mestra gerada deve continuar projetos antigos lendo `_CLAUDE/projeto.json` no local, sem movê-lo nem renomeá-lo.

Ao iniciar ou retomar a montagem do fluxo:

1. Procure `montagem.md` na pasta de ferramentas informada. Se a pasta ainda não tiver sido informada, pergunte onde está antes de procurar.
2. Se encontrar, mostre em 3 a 5 linhas a fase atual, as escolhas importantes, o que já foi escrito e o próximo passo.
3. Retome do ponto salvo. Não repita entrevista nem substitua arquivos já aprovados.
4. Se a pasta foi informada e não houver `montagem.md` nela, comece pela fase 0; não use o estado de um vídeo (`projeto.json`) como checkpoint da montagem.
5. Ao fim de cada fase, atualize `montagem.md`. Se essa gravação sair da pasta de trabalho autorizada, peça autorização antes.

## Fase 0 — Apresentar

Leia references/guias/principios-do-fluxo.md. Explique em poucas linhas:

- esta skill monta um fluxo pessoal; não edita o vídeo;
- no fim haverá skills próprias, incluindo uma skill mestra que a pessoa nomeia e invoca com $nome-da-skill;
- o processo passa por ambiente, entrevista, referências, plano, escrita das skills e teste com um clipe curto;
- é possível pausar e retomar usando $fluxo-de-edicao;
- as skills ficam em texto e podem ser lidas e alteradas.

## Fase 1 — Ambiente

Sem instalar nada, identifique o sistema operacional, Python, FFmpeg, Node.js, Git, ferramentas de edição e recursos de GPU quando forem relevantes para o fluxo. Use o terminal ou ferramentas disponíveis no Codex dentro do projeto autorizado. Mostre o que foi observado e o que está ausente; não finja ter verificado algo que não conseguiu consultar. Instale apenas as ferramentas escolhidas na fase 2, depois de explicar e obter autorização.

## Fase 2 — Entrevista

Leia references/guias/decisoes.md e siga a ordem. A primeira decisão é sempre onde a pessoa revisa: em um programa de edição ou assistindo ao vídeo renderizado. Essa escolha muda o fluxo todo.

Converse sobre tipo e formato do vídeo, padrão de pastas, transcrição e notas faladas, motion, câmera, som, revisões e ferramentas. Pergunte também onde as skills geradas devem ficar:

- projeto atual: `<pasta do projeto>/.agents/skills/`;
- todos os projetos do usuário: `~/.agents/skills/`.

Explique a diferença. Grave a escolha e o motivo em montagem.md. Se uma etapa depende de informação que a pessoa ainda não tem, registre como pendente e siga quando possível.

## Fase 3 — Referências e perfil

Leia references/guias/referencias.md. Ajude a pessoa a reunir trechos de vídeos de que gosta, identifique características de imagem, movimento, corte e som e escreva o perfil dela. Sem referências, os resultados tendem a ficar genéricos; recomende reunir algumas, mas permita começar com um perfil simples e completá-lo depois. Não atribua ao usuário um estilo que ele não escolheu.

## Fase 4 — Plano do fluxo

Proponha etapas a partir das oito referências abaixo, adaptando às respostas:

1. iniciar: abre o projeto e organiza o briefing;
2. preparar: inventaria mídia, sincroniza, transcreve com tempo por palavra e organiza notas faladas;
3. cortes: escolhe takes, remove erros e pausas e entrega o primeiro corte;
4. motion-mapa: planeja animações e câmera, sem animar;
5. assets: lista e obtém logos, ícones e capturas necessários, respeitando licenças;
6. motion-render: constrói e renderiza cada animação;
7. câmera: planeja zooms e movimentos sincronizados à fala e às animações;
8. sfx: organiza efeitos sonoros em camadas e sincronizados à imagem.

Inclua a skill mestra e as regras comuns. Adapte quando fizer sentido: Reels pode juntar etapas; vídeo sem animação pode pular 4 a 6; sem programa de edição pode ganhar uma etapa de render final. Explique a lista final, uma linha por etapa, e aguarde aprovação antes de criar as skills. Combine um prefixo curto em nomes válidos para Codex, com letras minúsculas, números e hífens. A skill mestra não pode ter o nome fluxo-de-edicao.

## Fase 5 — Escrever as skills

Na ordem: regras comuns, skill mestra e uma etapa por vez.

1. Leia o modelo e o guia da etapa em references/modelos/ e references/guias/. Leia também os guias de motion e entrega quando se aplicarem.
2. Separe ofício, que vale para qualquer vídeo, do gosto pessoal, que fica no perfil.
3. Gere uma skill por diretório, com SKILL.md e os materiais auxiliares de que ela precisa. Use o escopo que a pessoa escolheu: <pasta do projeto>/.agents/skills/<nome>/ ou ~/.agents/skills/<nome>/. Antes de gravar em ~/.agents/skills/, confirme autorização e o caminho.
4. Mostre um resumo curto do que a skill faz, salvo se a pessoa pedir o arquivo inteiro, e atualize montagem.md.
5. Preserve as versões existentes. Se o nome ou caminho já existir, explique a colisão e peça autorização para substituir ou escolha outro nome.

Scripts são descritos primeiro: o que fazem e quais armadilhas devem evitar. Escreva scripts somente na primeira execução real da etapa num vídeo, valide-os com esse vídeo e guarde-os na pasta de ferramentas. Não crie scripts especulativos durante a montagem.

Para cada entrega de arquivo novo para o programa de edição, a primeira execução deve gerar um exemplo curto para a pessoa abrir e conferir. Só continue depois da confirmação dela.

## Fase 6 — Teste com um clipe curto

Peça um clipe de 1 a 3 minutos, que pode ser gravado apenas para isso. Percorra o fluxo junto com a pessoa, etapa por etapa, pela skill mestra. É durante esse uso que os scripts reais são escritos, validados e os primeiros aprendizados são anotados. Corrija as skills somente com autorização da pessoa.

## Fase 7 — Fechamento

Comece o resumo com a instrução para usar o fluxo: abrir o projeto de vídeo no Codex e invocar $nome-da-skill-mestra. Ela lê o estado e recomenda a próxima etapa.

Depois mostre as skills criadas, a pasta onde foram gravadas, o ciclo de revisão e o caderno de aprendizados. Uma conversa nova no Codex é opcional; quando a pessoa iniciar uma, a skill mestra recupera o andamento pelo arquivo de estado. Marque a montagem como concluída em montagem.md. Para alterar o fluxo, use $fluxo-de-edicao e registre o novo escopo antes de mexer nos arquivos.
