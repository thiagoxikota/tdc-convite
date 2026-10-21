# Laboratório: convite para equipe

Abra os arquivos no navegador. Não precisa instalar nada, subir servidor nem ter conta de IA. Nenhum convite real é enviado.

**Durante a aula, escreva seu cartão e ouça um contraexemplo antes de abrir os patches.** Esta pasta é comparação posterior, não um gabarito para preencher a regra.

## Arquivos desta pasta

| Arquivo | O que é |
|---|---|
| `b-patch-trava.html` | Cópia de B com um patch escrito à mão: e-mail e perfil travam enquanto o convite está a caminho. |
| `b-patch-recibo.html` | Cópia de B com um patch escrito à mão: os campos ficam livres e o recibo histórico registra que eles mudaram durante a espera, mesmo se depois voltarem ao valor original. |
| `referencia.html` | Implementação didática completa, feita para a aula. Trava os campos durante a espera. |
| `base-inicial.html` | Tokens, API simulada e painel, sem formulário. A mesma base usada para gerar A e B. |

Nenhum destes arquivos é saída gerada por IA. Os patches estão rotulados no topo da página. As saídas A e B estão em `../demonstracao/`.

## Painel do laboratório

Abra **Painel do laboratório**, abaixo do formulário. Ele mostra quantas chamadas a API recebeu e o e-mail, perfil e estado da última.

| E-mail | Resultado depois de 1,2 s |
|---|---|
| `novo@example.com` | Sucesso |
| `ana@example.com`, `bruno@example.com` | Sucesso |
| `existe@example.com` | A pessoa já está na equipe |
| `falha@example.com` | A primeira tentativa falha; a segunda funciona |

Recarregue antes de cada teste. No teste de falha, não recarregue entre as duas tentativas.

## O teste da janela

1. Recarregue. Escolha Leitor e envie `ana@example.com`.
2. **Durante a espera**, troque o perfil para Editor ou apague o e-mail.
3. Leia a tela inteira quando a resposta chegar.

Após duas tentativas sem capturar a janela, use `../ensaio.html` e registre “reprodução didática observada”. Esse apoio de quatro segundos não executa os patches nem substitui testes de falha ou outros contraexemplos.

| Arquivo | Resultado |
|---|---|
| `../demonstracao/convite-b.html` | O select diz Editor e a frase confirma o envio como Leitor. O envio está correto; compare a apresentação com a regra que você escreveu. |
| `b-patch-trava.html` | Não dá para editar durante a espera. Compare com sua regra e com o custo de fazer a pessoa aguardar. |
| `b-patch-recibo.html` | A frase confirma Ana como Leitor e registra que os campos mudaram durante a espera. Ela não afirma que os campos atuais continuam diferentes. Compare com sua regra e com o custo da mensagem adicional. |

Se B já atende à sua regra, registre que passou e guarde o teste como regressão. Se a regra exige outra relação entre recibo e rascunho, registre o comportamento esperado, mostre a diferença em B e só então compare o patch. Outra regra é permitida; escrevê-la não prova que foi implementada.

## O cartão em vinte minutos

Cinco minutos para regra, custo e resultado observável; cinco para o chat procurar contraexemplos; oito para testar B; dois para revisar o cartão. Os patches entram depois da prática, quando o facilitador mostra a trava e o recibo. Ao sinal, mande a regra e o custo no chat; o facilitador lê alguns cartões, e quem tentar quebrar uma regra responde com o nome de quem escreveu e os passos. Quem preferir não postar revisa o próprio cartão.

O cenário de resposta perdida depois de uma escrita é discussão posterior. A simulação não tem servidor e não prova idempotência.

## Para gerar a sua versão (opcional)

Cole o seu cartão da janela no fim de `../demonstracao/pedido-b.txt`, use uma conversa nova e espere no máximo 4 minutos. Rode o teste da janela na primeira saída. Se a IA mudou a API simulada ou o painel, o resultado não é comparável.
