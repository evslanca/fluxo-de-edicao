# Princípios do fluxo

Boas práticas para produzir vídeos com consistência, sem impor um estilo único. Use-as nas regras comuns e nas skills de etapa.

## 1. Uma skill por etapa, uma etapa por vez
- Uma etapa tem uma responsabilidade clara. O fluxo só avança quando a pessoa aprova a etapa anterior.
- Se uma saída aprovada mudar, avise quais etapas dependentes precisam ser revistas antes de seguir.
- Não encadeie etapas sem a pessoa confirmar o próximo passo.

## 2. Planejar inteiro, executar por partes
- Cortes e mapa de animações precisam considerar a narrativa inteira.
- Render, câmera e som podem ser feitos por trechos escolhidos pela pessoa. Cada item pertence ao trecho em que começa.
- Cada trecho consulta as decisões dos anteriores para evitar repetir fórmulas.

## 3. A memória fica nos arquivos
- Cada vídeo tem uma pasta de trabalho _EDICAO/ e um estado projeto.json com decisões, status e pendências.
- O estado permite continuar na mesma conversa ou em uma conversa nova no Codex.
- Leia o estado pelo script de resumo em vez de despejar um arquivo grande no chat. Consulte apenas os blocos necessários.

## 4. O Codex decide; scripts calculam
- O assistente decide questões editoriais como escolha de take, entrada de animação e intenção sonora.
- Scripts fazem cálculos repetíveis: tempo por palavra, frames, bordas de corte, keyframes, níveis de áudio e formatos de entrega.
- Um script escrito para um projeto fica na pasta de ferramentas e só é reutilizado quando o formato e a finalidade forem compatíveis.

## 5. Ponto salvo, pendência e conversa nova
- Um ponto salvo existe quando o trecho ou etapa foi revisado, a saída gerada e o estado atualizado.
- Só nesse momento sugira continuar para a próxima etapa ou, se a pessoa quiser, abrir uma nova conversa e invocar a skill mestra.
- Pendências são registradas no estado até serem resolvidas.
- Nunca sugira abandonar uma conversa enquanto houver revisão não aplicada ou não registrada.

## 6. Caderno de aprendizados
- Registre correções, elogios e preferências que podem servir a outros vídeos.
- Ajustes exclusivos deste vídeo não viram regra geral. Se houver dúvida, marque-os como possivelmente específicos.
- Anotar não significa alterar o perfil ou as skills. Só aplique aprendizados quando a pessoa pedir, mostre a proposta e grave apenas o que ela aprovar.

## 7. Gosto separado do ofício
- Ofício que vale para qualquer vídeo fica nas skills.
- Preferências pessoais de cor, fonte, zoom, animação e som ficam em perfis próprios.
- Um projeto pode usar mais de um perfil sem duplicar o fluxo.

## 8. Tendência, não regra
- Princípios criativos são pontos de partida, não obrigações que tornam todos os vídeos iguais.
- Regras técnicas de sincronia, nível de áudio e formato podem ser firmes quando aprovadas.

## 9. Segurança
- Nunca mova, renomeie ou apague arquivos originais do projeto.
- Grave saídas na pasta de trabalho _EDICAO e use versões novas em vez de sobrescrever entregas existentes.
- Se um arquivo precisar sair de circulação, coloque-o em uma pasta de espera e deixe a exclusão para a pessoa.
- Alterações nas skills, scripts e perfis precisam de autorização explícita e devem manter histórico de versões quando houver Git.

## 10. Conferir formatos novos
- Antes de depender de um formato de entrega, crie um exemplo curto e peça para a pessoa conferir no editor.
- Se não souber como o programa representa algo, peça uma amostra exportada pelo próprio programa em vez de inventar o formato.
- Depois de alterar um script usado, compare a saída com um caso conhecido antes de substituir o fluxo aprovado.

## 11. Uso cuidadoso do contexto
- A pessoa pode continuar na conversa atual ou iniciar outra quando fizer sentido. O estado do projeto é a referência para retomar.
- Leia resumos e recortes: transcrição por frase, blocos selecionados do estado e um quadro apenas quando houver dúvida visual.
- Quando uma operação longa ainda estiver em andamento, acompanhe o resultado informado pela ferramenta; não reinicie o mesmo trabalho sem motivo.
- Escolha modelo e esforço entre as opções realmente disponíveis no Codex, conforme a complexidade da etapa. Não fixe nomes de modelos que podem deixar de estar disponíveis.
