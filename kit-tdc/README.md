# Laboratório: convite para equipe

Abra os arquivos no navegador. Não precisa instalar nada, subir servidor nem ter conta de IA. Nenhum convite real é enviado.

## Arquivos desta pasta

| Arquivo | O que é |
|---|---|
| `b-patch-trava.html` | Cópia de B com um patch escrito à mão: e-mail e perfil travam enquanto o convite está a caminho. |
| `b-patch-recibo.html` | Cópia de B com um patch escrito à mão: os campos ficam livres e a resposta avisa quando eles mudaram depois do envio. |
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

| Arquivo | Resultado |
|---|---|
| `../demonstracao/convite-b.html` | Falha: o select diz Editor e a frase diz "perfil Leitor". |
| `b-patch-trava.html` | Passa: não dá para editar durante a espera. |
| `b-patch-recibo.html` | Passa: a frase diz que o convite foi para Ana como Leitor e que os campos mudaram depois. |

## Para gerar a sua versão (opcional)

Cole o seu cartão D1 no fim de `../demonstracao/pedido-b.txt`, use uma conversa nova e espere no máximo 4 minutos. Rode o teste da janela na primeira saída. Se a IA mudou a API simulada ou o painel, o resultado não é comparável.
