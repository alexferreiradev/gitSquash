# Geral
Teste de `git merge --squash` na prática. 

# Unificar commits em git merge

O Assembla lista todas mensagens de commits na descrição do ticket. Fazer muitos commits em um ticket dificulta para quem quer ver o histórico de comentários. A solução encontrada foi usar o:

`git merge --squash`

Através do parâmetro --squash é possível fazer merge entres branches sem adicionar os commits para o branch final.

# Exemplo de uso

Suponha que você esteja trabalhando em um branch hot_fix123. Você cria um branch hot_fix123_history e realiza vários commits diários que são necessários para implementar a correção. Após finalizar a implementação, você realiza o merge para o branch hot_fix123 com --squash ativado. Dessa forma, os arquivos e alterações feitas no hot_fix123_history irão aparecer como novas modificações para serem comitadas para o hot_fix123.

Finalmente, você faz o commit no hot_fix123 com a mensagem: "Correção de conversão de data de aniversário, removendo o tempo do formato final". No Assembla, irá aparecer somente a mensagem final, e não os 50 commits que fez no branch hot_fix123_history.

# Uso no IntelliJ

No IntelliJ pode ser feito como na imagem em anexo, acesse VCS -> Merge Changes e marque o checkbox stash e faça o merge.
