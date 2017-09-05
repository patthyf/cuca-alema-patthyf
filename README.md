#Desafio 3 – Cuca Alemã

1. Aceitar a tarefa no link a seguir disponível na nossa sala do GitHub:


2. Você irá criar um lista com opções de cucas a serem escolhidas pelo usuário. Boa parte do trabalho HTML e CSS já está pronto. Espera-se que você modifique os seguintes arquivos para concluir essa tarefa:

a) index.html: Modificar para abrir em dispositivos móveis e para utilizar JavaScript.
b) style.css: foram definidos vários seletores em style-inicial.css, mas você deve modificar várias partes. Utilize o arquivo style.css e não o style-inicial.css para fazer essa modificações.
c) script.js: Coloque seu código JavaScript nesse arquivo.

1. Grid de opções:

As imagens devem ficar com o mesmo tamanho, uma ao lado da outra na mesma linha e na próxima linha automaticamente quando não couber na largura da página.
As caixas de marcação devem ficar no canto inferior esquerdo, logo após a figura.
Deixar um espaçamento de 20 pixeis entre as linhas.
Utilizar um flexbox multi-linhas para criar esse leiaute.
Cada item flex deve possuir uma largura de 32,5%, incluindo a borda,  e deve preencher o espaço existente no container flex
Cada container flex deve possuir cor de fundo #f4f4f4, borda de 1px thick e de cor #dcdcdc
O espaço entre a borda e o conteúdo deve ser de 10 pixeis.
A imagem para a caixa de marcação “desmarcada” está em imagens/unchecked.png
A altura e largura da caixa de marcação é de 20 pixeis.
Atenção: não usar o campo <input type=”checkbox” />, apenas mostrar a imagem fornecida.

Dispositivos Móveis:

Se a página for vista em um dispositivo móvel, o viewport deve ser setado para zoom-level 100% e a largura deve ser da largura do dispositivo.
Se o tamanho da tela do dispositivo for menor que 700 pixeis, a largura do conteúdo da página deve ser de 95% ao invés de 700px e os círculos amarelos no cabeçalho da página não devem aparecer.
Se o tamanho da tela do dispositivo for menor do que 500 pixeis, cada opção deve ocupar 49% de largura ao invés de 32,5%.

Comportamento da Página:

Esse desafio pede que o usuário escolha três opções de acordo com sua preferência. Escreva o código para que a página tenha o comportamento descrito a seguir.

Atributos Dataset
Você deve utilizar atributos datased adicionados aos elementos HTML no index.html:
- data-choice-id: Mapeia  qual resultado deve ser contabilizada, definida em constantes.js.
- data-question-id: Mapeia para o número da questão: um, dois e três.

Você pode utilizar esses atributos em JavaScript usando .dataset.choiceId e .dataset.questionId.
E pode acessar esses atributos pelos seletores CSS  [data-choice-id='tradicional'] e [data-question-id='dois'].

Ao clicar na Resposta
Quando o usuário clica em uma opção, ela deve marcar que aquela opção foi selecionada e desativar as outras opções da mesma pergunta.

Para o item selecionado, a imagem da caixa de marcação deve ser alterada de desmarcada para marcada. A cor de fundo deve ser #cfe3ff e a imagem deve ser alterada para imagens/checked.png.

Para itens não selecionados, devem ficar semi-transparentes, alterando sua opacidade para 0.6. Atenção para alterar o estado apenas das alternativas não selecionadas da mesma pergunta.

Alterar a Resposta
Caso o usuário não tenha respondido todas as questões, eles devem poder alterar sua resposta das questões já respondidas clicando em uma outra resposta. Após responder a todas as perguntas, as respostas devem ficar bloqueadas sem que possam ser alteradas pelo usuário, até que clique no botão “Reiniciar”, ou atualizar a página.

Completar o Questionário
Após o usuário ter respondido as três questões, o questionário está completo. Assim, não deve permitir selecionar uma nova alternativa. A personalidade da pessoa deve aparecer no final da página, com a personalidade correspondente as suas escolhas, conforme definido no arquivo constantes.js.

Pontuação
O data-choice-id  para cada alternativa mapeia para a chave  dos resultados possíveis em RESULTS_MAP, armazenado em constantes.js. Você pode acessar RESULTS_MAP em script.js porque o arquivo constantes.js foi incluido antes de scripts.js no arquivo index.html.

Quanto o questionário é completado, você pode pontuar o questionário contando o data-choice-id de cada resposta, considerando os quatro primeiros caracteres.  Por exemplo, se um usuário escolher intp-chocolate, infp-isopor e intp-granulado, perceba que ele escolheu duas respostas que começam com intp e assim, você deve mostrar o título e o conteúdo de RESULTS_MAP['intp'].

Se não houver uma maioria de tipos, você deve considerar a resposta da primeira pergunta apenas. Por exemplo, se o usuário escolheu estp-uva, enfj-frozen e isfp-crambery, você deve mostrar o título e o conteúdo de RESULTS_MAP['estp'].

Reinicar
Quando o usuário clicar em em reiniciar, a página deve retornar ao seu estado inicial.
As respostas devem ser desmarcadas
A personalidade deve desaparecer da tela
As alternativas devem ser ativadas e permitir que o usuário as marque novamente
Não pode atualizar a página (refresh)
Posicionar no início da página



