⬅️[Voltar para página inicial]()

# Introdução

O processo de Code Review (CR) é importante no desenvolvimento de software pois busca imbuir o código com maior qualidade através da visão de desenvolvedores que não participaram do processo de desenvolvimento. Desta forma, erros, padrões divergentes e vícios de implementação podem ser mitigados entretanto, para um CR eficiente, alguns processos e atividades devem ser aplicados. 
___
# Checklist de Code Review
Os passos abaixo devem ser seguidos no processo de CR, para atingir o máximo de aproveitamento da revisão. Lembre-se, você está revisando um código que agregará valor ao cliente. Da mesma forma, um código bem revisto evita retrabalho e bugs. Os passos são:

1. Verifique se há conflitos: Verifique se o PR gera algum conflito de código. Em caso positivo, solicite ao autor a correção imediatamente.
2. Leia o conteúdo do Pull Request (PR): Ao efetuar uma CR, leia o conteúdo do PR. Dessa forma você saberá o objetivo do código desenvolvido, passo imprescindível para entendê-lo.
3. Verifique os Work Items (WI) ou Cards vinculados: Ao verificar os WI's, você obterá ainda mais informações sobre o código desenvolvido. 
4. Verifique os parametros de AutoComplete: Verifique os parametros de autocomplete selecionados. Desta forma, evita PR's completados com parametros incorretos. Verifique:
- Se a opção de merge selecionada é "Merge (no fast forward)".
- Se a opção de deletar branch de origem está marcada caso disponível. Exceto para PR's de branches principais (release para develop, develop para main, etc).
5. Leia as tags presentes no PR caso existam.
6. Verifique se o código é construido corretamente: Verifique se o build do código acontece sem erros. Na ausencia de pipelines de pré-deploy, faça o checkout da branch utilizada no PR e execute o build localmente.
7. Verifique se o código foi analisado no Sonarlint: No PR haverá uma opção marcada caso o desenvolvedor tenha executado a análise. Em caso contrário, se possível, faça o checkout da branch utilizada localmente e execute a análise.
8. Faça uma primeira leitura do código observando apenas as alterações criadas.
9. Leia os arquivos modificados um por um, na integra: dessa forma você ganha o contexto do objetivo de cada arquivo, assim como o antes e depois da alteração. 
10. Observe os pontos a seguir durante a leitura do código:
- Design: O código criado apresenta o design indicado, tanto pela literatura da linguagem quanto os padrões adotados no time?
- Funcionalidade: O código criado funciona conforme o esperado? Há pontos de melhoria?
- Complexidade: O código criado aumenta a complexidade do algoritmo? Há outra abordagem para tratar este caso?
- Testes: O código criado apresenta testes unitários? Estes são eficientes? A cobertura é satisfatória?
- Nomeclaturua: As variáveis, classes e métodos possuem nomes que seguem as convenções de linguagem ou do time?
- Comentários: Existem comentários no código? Eles são necessários?
- Estilo: O código segue o guia de estilo da linguagem utilizada?
- Documentação: O código está devidamente documentado?
- Tratamento de exceções: O código apresenta tratamento de exceções para todos os casos necessários?
- Contexto: Dentro do contexto da aplicação e da mudança proposta, o código supre as expectativas? Há pontos de melhoria?
- Boas práticas: O código segue as boas práticas da linguagem, comunidade ou time?
11. Deixe comentários: Em caso de dúvidas, não conformidadades ou elogios ao código criado, deixe comentários na linha exata onde necessita-se de mudança ou onde pretende-se elogiar.
12. Aprove ou bloqueie a aprovação do PR: para dar sequencia ao processo do PR, siga os passos a seguir:
- Caso o código cumpra o seu objetivo e atenda todos os pontos supracitados, aprove o PR.
- Caso tenha deixado algum comentário com sugestões a serem analisadas ou pontos a serem corrigidos, selecione a opção "Wait for author" e cancele o autocomplete.
- Caso o PR tenha algum erro grave de código, ou coloque a segurança e estabilidade da aplicação em risco, rejeite o PR.
13. Revise os pontos ajustados: Após o autor incluir as correções ou sugestões sugeridas, revise os pontos conforme as orientações acima. Caso todas tenham sido atendidas, aprove o PR.
___
# Orientações para Execução do CR

Neste item, serão listadas algumas atitudes que contribuirão para um processo de Code Review mais tranquilo, assertivo e sem conflitos.
- Faça o processo de CR com calma. Reserve tempo para ler o conteúdo do PR e os códigos, para ter uma melhor visão do contexto.
- Em caso de dúvida, deixe comentários ou comunique com o autor.
- Não faça alterações no código sem alinhamento com o autor. Em caso de necessidade, alinhe com ele que você fara as alterações e peça a outra pessoa para efetuar o CR. 
- Só rejeite um PR em caso de risco. Do contrário, solicite as alterações ao autor. Caso um PR seja rejeitado, selecione a opção "Abandon" em seguida.
- Caso haja alguma dúvida sobre o procedimento ou codificação, entre em contato com o sênior da squad, ou com os líderes técnicos.
- Caso seja incontornável a necessidade de fazer um PR grande, e mediante a apresentação de uma justificativa, a revisão deste deve ser feita de forma síncrona, em chamada envolvendo o autor e os revisores, para agilizar o processo.
- PR's grandes sem justificativa devem ser rejeitados, para que sejam divididos pelo autor e facilitar assim o processo de Code Review.
- Aprovação de sênior ou Tech Lead e contexto da atividade: Os PR's devem ser aprovados por, no mínimo, 2 avaliadores sendo 1 deles sênior ou líder técnico, e que este esteja no contexto da atividade desevolvida, para trazer clareza e entendimento à revisão.
___
# Orientações para Comentários
Alguns pontos devem ser levados em consideração durante a comunicação do revisor com o autor. Esta comunicação deve ser clara, concisa e respeitosa. Alguns cuidados devem ser tomados nessa comunicação, principalmente ao que diz respeito aos comentários em uma CR:
- Faça comentários curtos e precisos. Não é necessário efetuar comentários estensos. Caso necessário, entre em contato direto com o autor.
- Em caso de sugestões, apresente-as com pequenos trechos de código ou links para orientar o autor.
- Prefira usar linguagem sugestiva à imperativa. Ao invés de utilizar um comentári como "Ficou ruim", prefira "é uma boa prática utilizar nomes mais descritivos" e apresente sugestões.
- Utilize perguntas para trazer reflexão ao autor. Exemplo : "É mais interessante utilizarmos o padrão do MVC. Você consegue perceber as melhorias associadas?".
- Seja cordial e educado. Lembre-se, você está avaliando o código, e não o autor. O objetivo é manter a qualidade e eficiência do projeto.
- Faça elogios à códigos eficientes. Elogios são ótimas formas de incentivar uma pessoa a se dedicar. Por isso, ao ver um código bem executado, não refreie-se de elogiá-lo.
- Inserir razão do comentário: para trazer mais clareza à necessidade, descreva a razão deste. Desta forma o autor consegue identificar melhor a necessidade da mudança proposta.
- Inclusão de exemplo: ao criar um comentário, busque inserir exemplo da mudança sugerida, se possível. Tal abordagem facilitará a correção por parte do autor.
- Revise e comente independente da senioridade: todos podem revisar e criar comentários em PR'S. Além da melhoria do código, também é um momento de troca de experiencia. Mesmo um júnior revisão código de um sênior, deve fazer comentários caso achei necessário. Lembrando sempre de manter em vista o tato e a cordialidade.

___
# Referências
[Review pull requests](https://learn.microsoft.com/en-us/azure/devops/repos/git/review-pull-requests?view=azure-devops&tabs=browser)
[How to do a code review](https://google.github.io/eng-practices/review/reviewer/)
[Boas práticas para utilizar no code review](https://www.linkedin.com/pulse/6-boas-pr%C3%A1ticas-para-utilizar-code-review-leticia-coelho/?originalSubdomain=pt)
[conventional: comments](https://conventionalcomments.org/)
