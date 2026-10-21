# Registro da demonstração A/B

## Procedência

Gerado em 19/10/2026, durante a preparação deste workshop, em duas sessões independentes do Codex, sem histórico da outra condição e instruídas a ler só o próprio arquivo de entrada.

- Sessão A: entrada integral `pedido-a.txt`, primeira implementação `convite-a.html`.
- Sessão B: entrada integral `pedido-b.txt`, primeira implementação `convite-b.html`.
- Modelo: **não informado pela ferramenta**. As sessões usaram a configuração herdada, sem override. Não atribua identificador nem parâmetros que a ferramenta não expôs.
- Mesma base, tokens, painel e API. Uma geração por condição. Nenhuma saída foi escolhida por qualidade, corrigida depois ou trocada por um exemplo pior.

Este par foi preparado antes da aula. Não é uma geração feita diante da turma e não mede com que frequência o resultado se repete.

## Integridade

Os dois HTMLs são cópias byte a byte dos arquivos de 19/10.

| Arquivo | SHA-256 |
|---|---|
| `convite-a.html` | `4dbcec3aac7de1d58b964d0e61a3a521b970c55a44db31280f0454e9ae4fd06d` |
| `convite-b.html` | `931571a1406ef704385f4aa8d9b3255fd87a7eb7381feb9e97de13dd5d8a5e4b` |
| `../kit-tdc/base-inicial.html` | `87e2bd4c7493ad02703a17a7d93cf0db961064c667f9f68e930159505825ed64` |

O script da API (`b6da5891ea6511c79dbfbf4c5a830db0c6d9407c6abf016ac6080f0dd80cec11`) e o HTML do painel (`083d45d4cf2c9ab2be2d0daf57e4864fa58fcb43ea33b3edd0fa4dd6994379fc`) são idênticos em base, A, B, referência e nos dois patches. `verificacao.json` é o registro original da verificação de 19/10, mantido sem edição.

## O que o Chrome mostra

| Teste | A | B |
|---|---|---|
| C10 contexto | Não cumpre: card centralizado, título promocional, sem a gestão de pessoas que o pedido A não citava. | Cumpre: bloco à esquerda, grid 2:1 a partir de 720 px. |
| C3 espera | Cumpre: uma chamada com clique e Enter repetidos. | Cumpre. |
| C6 falha | Cumpre: campos preservados, segunda tentativa funciona. | Cumpre. |
| D1 depois do sucesso | Não se aplica: A troca o formulário pela tela de sucesso. | Cumpre: editar limpa a confirmação. |
| Editar **durante** a espera | Campos desabilitados. Sem ambiguidade. | Campos livres. Envia Ana como Leitor, troca para Editor: o select diz Editor e a frase diz "perfil Leitor". |
| Foco depois da resposta | Puxa o foco para o título de sucesso, mesmo se você saiu. | Mantém o foco onde a pessoa está. |
| Perfil padrão | Membro | Leitor |

A janela de espera foi achada em 20/10, numa sonda nova sobre os mesmos arquivos. A verificação de 19/10 não testou esse caso. B cumpre D1 como foi escrita, porque o texto falava de "depois do sucesso". O intervalo ficou sem dono na especificação; não é bug retroativo de B.

## Onde olhar em `convite-b.html`

- **Linha 62:** media query de 720 px com grid 2:1 (C10).
- **Linha 173:** `let aguardando = false;`, o único estado da espera.
- **Linhas 188 a 199:** limpeza da confirmação ao editar (D1).
- **Linhas 216 a 218:** cópia dos campos para o envio e início da espera. O botão bloqueia; os campos, não.
- **Linhas 231 e 232:** a frase de sucesso usa o envio, não os campos atuais, e marca a confirmação.
- **Linha 239:** fim da espera.

## Limites

Um par de saídas não mede consistência nem isola o tamanho do pedido. B recebe mais informação de propósito. A API simulada aceita o perfil que recebe e não prova autorização de backend. Leitor de tela e zoom nativo de 200% não foram testados.
