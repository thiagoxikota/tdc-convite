# O que não entra na interface

Exemplo de lista para o AGENTS.md, o CLAUDE.md ou as regras do editor do seu time, junto do design system. É o que o agente lê antes de gerar ou alterar uma tela de ferramenta, aquela que a pessoa abre várias vezes por dia. Cada time escreve a sua. Mudou de ideia? Muda a lista num PR, com revisão.

## Não entra

- Sobretítulo em caixa alta acima do título.
- Slogan, frase de efeito e título motivacional. O título diz a tarefa: "Convidar pessoa".
- Ícone decorativo, ícone num quadradinho e ilustração sem função.
- Gradiente, sombra em card e card centralizado sozinho na página.
- Cor, raio ou espaçamento fora dos tokens.
- Componente novo quando o design system já tem um equivalente.
- Emoji em título, botão ou mensagem do sistema.
- Confete e animação de celebração.
- Campo, select ou perfil que o pedido não pediu.
- Adjetivo vago no pedido: moderno, intuitivo, poderoso, limpo.

## Sempre entra

- Copy real. Botão com a ação ("Enviar convite") e label visível em todo campo.
- Estados escritos: vazio, loading, erro, sucesso e sem permissão.
- O que fica editável durante o loading e o que a confirmação mostra depois.
- Foco previsível depois da resposta. Nada rouba o foco de quem saiu do form.
- Teclado completo e contraste dentro dos tokens.
- Teste com texto longo: nome grande, e-mail gigante.

## Como usar

Cole a lista no arquivo de contexto que o agente lê, ao lado do design system. Na revisão do output, confira item por item antes de perguntar se ficou bonito.
