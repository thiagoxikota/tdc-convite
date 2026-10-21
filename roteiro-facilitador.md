# Roteiro do facilitador · TDC Talks · 21/10/2026

19h às 20h30, Brasília. Noventa minutos previstos, incluindo demonstrações, participação e perguntas. Os tempos abaixo são um plano de condução, não uma duração medida em ensaio.

O núcleo é observar decisões deixadas abertas, escrever uma regra própria, admitir seu custo e verificar um comportamento. O cartão serve ao próximo refinamento ou PR. A e B são primeiras saídas preservadas. O bingo é um jogo; o par A/B não mede frequência nem isola causalidade geral. O payload de B está correto. A questão é qual relação a interface deve mostrar entre o recibo concluído e os campos que já mudaram.

## Antes da transmissão

- Abra o deck no mesmo navegador e modo de compartilhamento que usará na aula. Confira notas, escala e leitura do código.
- Abra A, B, os dois patches e `ensaio.html` em abas separadas, sem projetar respostas antes da hora.
- Baixe e extraia o ZIP. Abra o `index.html` extraído para conferir que o caminho offline está disponível.
- Ensaie D1: envie Ana, espere o sucesso e edite. A confirmação deve sumir em B.
- Ensaie a mudança durante o envio: foco no e-mail, Leitor, Enter, Tab, E. O select nativo pode variar. A demonstração tem uma janela de 1,2 segundo; não conte com a velocidade da plateia para garantir a revelação.
- Deixe a instrumentação de `ensaio.html` pronta como apoio. Identifique o modo lento/replay como ensaio didático separado de B original. Se a janela passar, mostre o apoio e continue; não gaste a sessão brigando com o teclado.
- Tenha o material local como apoio à projeção. Não afirme teste com leitor de tela, idempotência de backend ou geração ao vivo.

## Relógio

| Horário | Minutos | Bloco |
|---|---|---|
| 19h00–19h05 | 0–5 | Entrada no kit, promessa e regra de participação |
| 19h05–19h15 | 5–15 | Pedido, bingo, cartela revelada e A em dois estados |
| 19h15–19h27 | 15–27 | Testes de A, decisões de produto e ponte para comportamento |
| 19h27–19h40 | 27–40 | B, D1, falso encerramento, edição durante a espera e comparação com A |
| 19h40–19h45 | 40–45 | Antes/durante/depois e instrução da prática |
| 19h45–20h05 | 45–65 | Cartão, contraexemplo, teste, comparação e revisão |
| 20h05–20h15 | 65–75 | Defesa das regras, código e custos dos patches |
| 20h15–20h22 | 75–82 | Busca, resposta perdida e perguntas para o próximo refinamento ou PR |
| 20h22–20h30 | 82–90 | Perguntas |

Se houver atraso, reduza o debate inicial e o tempo de leitura de código. Preserve a prática e D1. O desafio de resposta perdida pode virar uma pergunta rápida, com a resposta disponível no material posterior. Encerre a atividade e abra perguntas às 20h22.

## Apostas: uma cadência para as quatro

1. Mostre a pergunta e explique o formato da resposta.
2. Peça que cada pessoa guarde a escolha. No bingo, as nove casas ficam privadas; depois da revelação, peça só o total de acertos. Nas outras apostas, todos enviam ao seu sinal para a primeira resposta não conduzir o resto da sala.
3. Conte os últimos segundos em voz alta. Diga “Valendo” para receber as respostas, espere uma janela curta de chegada e feche: “Votação encerrada”. Não espere unanimidade nem um placar perfeito.
4. Revele. Dê dois segundos para a sala reconhecer antes de explicar.
5. Ouça uma justificativa e conecte ao próximo teste. Não transforme cada aposta em uma palestra.

## Pedido e bingo

Abra com a costura do título, sem um bloco novo de teoria. Diga: “Moderno e responsivo descreve qualidades, mas não distingue as alternativas que servem ao nosso produto. Neste exemplo, vamos observar quais escolhas a IA completou e o que muda quando a equipe fornece contexto, restrições e uma regra verificável.” Apresente o pedido A inteiro na parte de produto. A base técnica é a mesma, com tokens, API simulada e painel; não diga que A foi criada sem contexto algum.

Na aposta, cada pessoa escolhe exatamente nove das doze casas e guarda a escolha. Não peça a transcrição das nove no chat. Depois da revelação, conta quantas armadilhas marcou. Acertos são nove menos esse número; peça só esse total ao sinal. Não use “sete ou mais” como evidência de previsibilidade nem infira que o treino do modelo explica o resultado. O placar serve à brincadeira.

Mostre a cartela revelada, os recortes de perfil e botão e o estado de sucesso de A. Abra o select para confirmar Membro e Administrador. Leia o título e o slogan ampliados no slide; um estado só não mostra todas as casas. A frase “Pedi um formulário. Veio um discurso de boas-vindas” cabe depois de a sala ler o título e o slogan. Se não houver reação, siga sem explicar a piada.

Faça a ponte: o pedido deixou decisões visuais abertas; vamos procurar uma decisão de comportamento que também ficou aberta. A fonte do contexto, num produto real, é o repositório, o design system, os contratos de API e o que a equipe já decidiu. No refinamento, produto e engenharia enfrentam as lacunas. O HTML isolado só deixa esses estados visíveis na bancada da aula; a decisão vai para a stack do produto.

## A funciona, e isso importa

Peça o palpite de zero a três antes dos testes. Explique o painel uma vez e recarregue entre cenários, exceto entre as duas tentativas de `falha@example.com`.

Mostre C3 e C6 funcionando. C10 avalia contexto de gestão que A não recebeu. Evite apresentar isso como descumprimento de A. A pergunta sobre Administrador é decisão de produto e permissão exposta na interface; o select não prova autorização no servidor.

Escolha uma decisão para debate curto. Pergunte a uma pessoa qual padrão adotaria e o que perderia com ele.

## B, D1 e a virada

Mostre D1 como foi escrita: depois do sucesso, editar limpa a confirmação. Envie Ana, aguarde e comece a editar. B passa. Diga “Especificou, funcionou. Obrigado, boa noite.” Pare por um instante. Só então avance para a aposta sobre editar durante a espera.

Feche a votação antes de executar o gesto. Revele o perfil atual, o perfil confirmado e o painel. Nomeie as três camadas: payload correto; recibo correto do envio de Ana; rascunho atual diferente. O critério adicional de apresentação ainda não foi decidido. Não diga que B convidou com o perfil errado.

Compare com A, que trava os campos sem isso ter sido pedido. Faça a pausa para a contradição aparecer. A também tem o comportamento de puxar foco; preserve o placar honesto.

## Prática de vinte minutos

Não mostre as duas soluções como escolhas prontas antes do cartão. Peça uma regra observável, não a palavra “seguro” ou “claro”. A pessoa precisa apontar a fonte do contexto, dizer o que pode editar, o que aparece no recibo e qual custo aceita. Quem atua em produto pode começar pela intenção e pelo resultado; quem desenvolve, pelos contratos, estados e código. Os dois lados desafiam e testam. Deixe explícito que qualquer papel participa sem implementar.

**Cinco minutos: escrever.** Cada dupla preenche o cartão. No remoto sem salas, cada pessoa escreve sozinha antes de ler o chat. Quem está sem computador acompanha a projeção e escreve no papel.

**Cinco minutos: adversário.** Outra dupla tenta quebrar a regra. No remoto, peça “Publiquem Regra + Custo”, selecione dois cartões e identifique os autores. Depois diga “Escolha um desses cartões e responda com nome do cartão + passos que tentam quebrá-lo”. Quem não publicar pode revisar o próprio cartão ou um dos selecionados. Proponha apenas se a sala travar: mudar duas vezes, voltar ao valor original, editar antes de uma falha ou tentar novo envio. Uma regra que resiste não precisa ganhar um defeito inventado.

**Oito minutos: testar.** Primeiro B, anotando o observado. Após duas tentativas sem capturar a janela, libere o ensaio de quatro segundos e peça o registro “reprodução didática observada”. Esse apoio não executa patches nem substitui testes de falha ou outros contraexemplos. Se a regra já existe, B passa e o teste vira regressão. Se exige outro comportamento, mostre o resultado esperado e a diferença. Só depois libere `respostas.html#patches` para comparar as implementações. Outra solução pode ficar especificada; não a chame de implementada se não foi executada.

**Dois minutos: revisar.** Atualizem o cartão e preparem a defesa de trinta segundos. Escolha duas regras diferentes para ouvir. Se a sala produziu trava e recibo, convide “time trava” e “time recibo”; se produziu outra decisão, use o nome escolhido pela pessoa.

## Defesa e código

Cada lado precisa dizer uma garantia e admitir um custo. O outro lado pode pedir um contraexemplo. Não existe vencedor obrigatório entre regras legítimas. O avanço é sair com um contrato mais verificável do que “componente moderno”.

Mostre o trecho do payload antes do `await` e o recibo depois. O campo pode mudar durante o intervalo. Não chame o problema de duas respostas de convite fora de ordem: o exemplo seguinte da busca tem esse mecanismo, mas este não.

Na comparação, travar implica aguardar para corrigir uma letra; recibo exige representar separadamente o envio e o novo rascunho. O complemento do recibo descreve a mudança ocorrida durante a espera e continua verdadeiro quando os campos voltam ao valor original. Mostre só as linhas necessárias e abra o fonte completo se alguém perguntar. Não leia todo o código projetado.

## Transferência: busca e resposta perdida

Na busca, explicite os instantes: `an` sai em 0 ms e `ana` em 100 ms. Com latências de 900 ms e 200 ms, chegam em 900 ms e 300 ms. Peça o que fica na tela e a regra, juntos. A lista de `an` chega por último e inclui Anderson. O contador impede essa resposta antiga de substituir a intenção atual. Se citar `AbortController`, diga que o `signal` precisa chegar ao `fetch` e preserve a identidade da requisição conforme a implementação.

No desafio sênior, diferencie o conhecimento do enunciado do conhecimento do navegador. Nós sabemos que o servidor gravou porque o cenário diz isso. O navegador viu apenas falha de rede. Precisa representar o resultado desconhecido e reconciliar. Repetir com segurança depende de contrato de idempotência/deduplicação no servidor, não de gerar outra chave a cada clique.

Identifique esse cenário como discussão fora da API simulada. Não improvise uma demonstração de backend inexistente.

## Fecho e perguntas

Recupere uma regra e um custo defendidos pela sala. Volte ao título: no pedido A, “moderno” deixava escolhas abertas; B explicitou contexto e critérios; o durante ainda exigiu uma decisão. Especificar deu critérios para avaliar a saída, inclusive com IA implementando. Peça que uma pessoa escolha um componente real do próprio trabalho e nomeie uma regra ausente, a fonte do contexto, o custo e um teste. O cartão pode ir ao refinamento, ticket ou PR. Entregue o link de respostas e encerre a atividade, mesmo que alguém esteja terminando.

Nas perguntas, preserve os limites: duas saídas, mesma base técnica, contextos de produto diferentes, uma geração cada, arquivos originais mantidos e modelo não informado. O bingo não muda essas limitações. Quando algo não foi testado, diga isso e aponte onde o material permite continuar depois.
