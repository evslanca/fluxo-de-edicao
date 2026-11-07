# Modelo: skill mestra

Crie esta skill em <escopo de skills escolhido>/<nome-da-skill-mestra>/SKILL.md. Ela coordena o fluxo, mostra o estado e encaminha para a skill de etapa. A pessoa invoca com $<nome-da-skill-mestra>.

---

```markdown
---
name: <nome-da-skill-mestra>
description: "Use quando a pessoa quiser iniciar, retomar ou consultar o estado de um vídeo neste fluxo."
---

# <nome-da-skill-mestra>

Fluxo: <etapa 1> → <etapa 2> → … → <última etapa>

Antes de encaminhar uma etapa, leia as regras comuns no caminho registrado em montagem.md.

## $<nome-da-skill-mestra>
1. Se não existir _EDICAO/projeto.json, procure _CLAUDE/projeto.json. Se esse estado legado existir, explique e pergunte se a pessoa quer continuar lendo-o no local. Não mova nem renomeie arquivos. Só ofereça $<prefixo>iniciar quando não existir projeto anterior e a pasta atual estiver correta.
2. Consulte o estado e mostre etapas, progresso por trecho, pendências, alertas e aprendizados.
3. Recomende uma próxima etapa e pergunte se a pessoa quer seguir. Só então use a skill correspondente.
   - Se uma etapa aguarda revisão, retome essa etapa antes de avançar.
   - Se o estado mostrar uma saída desatualizada, explique o impacto e espere uma decisão.
   - Se a pessoa pedir uma etapa específica ou um trecho, respeite o escopo pedido.
4. Trabalhe uma etapa por vez. Não encadeie etapas sem confirmação.
5. Lembre em uma linha o modelo ou esforço indicado para a etapa, se isso estiver documentado e disponível.

## Aplicar aprendizados
Quando a pessoa pedir, siga a seção correspondente das regras comuns e atualize o perfil ou skills somente após aprovação.

## Regras
- Esta skill não edita vídeo e não executa scripts de etapa.
- Não inicie uma nova conversa por conta própria. Ao fechar o checkpoint, a pessoa decide se continua aqui ou abre outro chat.
- Nunca mova, renomeie ou apague arquivos do projeto.
```
