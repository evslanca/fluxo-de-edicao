# Modelo: estado do vídeo e script de estado

Cada vídeo tem seu estado em _EDICAO/projeto.json. Esse arquivo é a memória durável do fluxo e permite retomar em outra conversa do Codex.

## Esqueleto

```json
{
  "projeto": "2026-01-15_Nome",
  "perfil": "<nome do perfil>",
  "ferramentas": { "hyperframes": "<versão usada neste vídeo>" },
  "etapas": {
    "iniciar": "concluido",
    "preparar": "concluido",
    "cortes": "aguardando_aprovacao",
    "motion_mapa": "pendente"
  },
  "midia": { "...": "arquivos, fps, proxies, sincronia e áudio principal" },
  "transcricao": { "...": "caminhos das transcrições e dos silêncios" },
  "notas_edicao": [ { "id": "n01", "texto": "usar este take", "etapa": "cortes", "interpretacao": "..." } ],
  "cortes": { "versao": 1, "segmentos": [ { "id": "s001", "video": "cam01", "inicio": 3.10, "fim": 15.62, "texto": "..." } ] },
  "marcadores": [ { "id": "m001", "video": "cam01", "tempo": 48.3, "tipo": "duvida_take", "texto": "..." } ],
  "motions": { "trechos": {}, "itens": [ { "id": "mo01", "status": "aprovado", "render": { "arquivo": "...", "versao": 1 } } ] },
  "camera": { "movimentos": [], "recortes": [] },
  "sfx": { "itens": [], "recortes": [] },
  "pendencias": [ { "id": "p01", "etapa": "motion_render", "texto": "mo05 mais lento" } ]
}
```

Status de etapa: pendente, em_andamento, aguardando_aprovacao, aguardando_<pessoa>, concluido ou nao_precisa.

Tempos de cortes e marcadores usam o tempo do arquivo de origem para sobreviver a versões novas da sequência. IDs estáveis permitem pedir ajustes sem ambiguidade.

## Script de estado

Escreva o script pequeno quando a primeira etapa real precisar dele; valide nesse projeto e use-o para consultar e alterar somente os blocos necessários:

- status: etapas, progresso, pendências e alertas;
- <bloco>: resumo legível; --json: bloco completo;
- --item <id>: um item;
- --set <caminho> <valor> e --etapa <etapa>=<status>;
- --pendencia <etapa> "<texto>" e --resolver <id>.

O script reduz leituras repetidas do estado inteiro. Não o escreva especulativamente durante a montagem do fluxo.
