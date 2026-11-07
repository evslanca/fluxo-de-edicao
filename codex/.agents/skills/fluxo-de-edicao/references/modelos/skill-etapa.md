# Modelo: skill de uma etapa

Crie em <escopo de skills escolhido>/<prefixo><etapa>/SKILL.md. O ofício vem de references/guias/etapa-*.md, adaptado às escolhas da pessoa. O gosto pessoal fica no perfil.

Mantenha a skill curta: entradas, saídas, procedimento, validação, revisão e regras. Coloque recursos de apoio ao lado do SKILL.md quando necessário.

---

```markdown
---
name: <prefixo><etapa>
description: "Use quando a pessoa pedir para executar ou revisar a etapa <etapa> do fluxo de edição."
---

# <prefixo><etapa>

<Descreva o que a etapa entrega e o que não faz.>

- **Lê:** <blocos do estado, briefing, perfil e saídas anteriores>
- **Escreve:** <bloco no estado e arquivos em _EDICAO/>
- **Próximo passo:** $<prefixo><próxima-etapa>

Se a etapa anterior não estiver concluída, pare e sugira terminá-la.

## Ofício
<Princípios da etapa. Decisões criativas são tendências; decisões técnicas podem ser firmes.>

## Perfil
<Arquivos do perfil a consultar e o que cada um determina.>

## Scripts
<Script, finalidade e armadilhas. Escreva e valide scripts somente na primeira execução real autorizada.>

## Passo a passo
1. Consulte o estado e as pendências desta etapa.
2. <…>
3. Gere a entrega. Na primeira vez, produza um exemplo curto para a pessoa validar antes do uso completo.

## Resumo no chat
Resuma o trabalho, o que exige atenção da pessoa e o caminho da entrega. Marque aguardando_aprovacao.

## Revisão
A pessoa pode apontar itens por ID, tempo ou retorno do editor. Altere só o escopo indicado, gere nova versão e anote aprendizados.

## Aprovação
Marque concluído, informe aprendizados anotados e sugira continuar nesta conversa ou, se a pessoa quiser, abrir nova conversa e invocar $<nome-da-skill-mestra>.

## Regras comuns
Leia o arquivo de regras comuns no caminho registrado em montagem.md.

## Regras
- Nunca mova, renomeie ou apague arquivos do projeto.
- Fale em português e seja direta.
```
