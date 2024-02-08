# Padrões de Desenvolvimento - vcnafacul

Bem-vindo ao repositório dos Padrões de Desenvolvimento da vcnafacul. Este documento descreve as diretrizes e boas práticas a serem seguidas pelos colaboradores ao contribuir para os projetos da organização.
Os guias descritos neste repositório visam orientar os profissionais voluntários no processo de trabalho do dia a dia do VcNaFacul. Este processo engloba a criação de commits de desenvolvimento, e as movimentações de cards do Board do Trello e o processo de Pull Request (PR) e Code Review (CD).
As propostas contidas aqui são orientações e estão abertas a mudanças a sugestões.

Criar card no trello vai se chemar numero do card e epico

## Git

- **Branches**:
  - Utilize o modelo de branching [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/) para gerenciar o fluxo de trabalho.
  - Mantenha nomes de branches descritivos e claros, evitando abreviações desnecessárias.
  - Feature/numero do card
  
- **Commits**:
  - Siga o estilo de mensagem de commit no formato: `<tipo>: <descrição>`.
  - Tipos comuns incluem `feat` (para novas funcionalidades), `fix` (para correções de bugs), `docs` (para alterações na documentação), `chore` (para tarefas de manutenção), entre outros.
  
- **Pull Requests**:
  - Crie Pull Requests claros e concisos, descrevendo as alterações realizadas.
  - Garanta que o código esteja revisado por pares antes de fazer merge.
  - numeração do card no começo do 

## Linguagem

- **Padrão de Codificação**:
  - Siga as diretrizes de estilo da linguagem escolhida (por exemplo, PEP 8 para Python).
  - Utilize nomes de variáveis e funções descritivas e significativas.

- **Documentação**:
  - Documente o código de forma clara e concisa.
  - Utilize comentários para explicar trechos de código complexos ou não triviais.

## Issues

- **Criação de Issues**:
  - Descreva as issues de forma clara, indicando o problema ou a melhoria desejada.

- **Atribuição de Issues**:
  - Atribua as issues a si mesmo ou a outros colaboradores, conforme apropriado.
  
- **Labels**:
  - Utilize labels para categorizar as issues, facilitando a identificação de áreas de trabalho.
 
# Licença

Queremos sempre usar a Licença do MIT nos novos projetos para que o projeto seja open-source e seja referenciado quando utilizado.

## Contribuições

- **Diretrizes para Contribuições**:
  - Antes de contribuir, verifique se há issues abertas relacionadas à sua contribuição.
  - Siga as diretrizes de estilo e formatação estabelecidas neste documento.
  - Ao enviar uma Pull Request, inclua uma descrição clara das alterações realizadas.

## Contato

Para mais informações ou dúvidas, entre em contato com os mantenedores do projeto.

---

**Nota**: Estas diretrizes são sujeitas a alterações e podem ser atualizadas conforme necessário. Verifique regularmente este documento para obter as últimas informações.

Resoluções adicionais - Fluxo de trabalho, commits, Pull Requests e Code Review
Olá pessoal. Inalgurando o canal tech aqui.
 
Diante das abordagens para melhoria dos processos de commit, Pull Request e Code Review, gostaria aqui de informar as últimas resoluções que devem ser adotadas. Tais resoluções serão incorporadas à documentação já existente, que oriento a todos a lerem e adotarem as práticas lá sugeridas. A documentação esta neste link.
Para dar maior visibilidade, vou descrever os itens a seguir:
Commits em inglês por padrão: somos uma empresa multinacional, e o objetivo dos commits e gerar um changelog das aplicações modificadas. Como esta documentação poderá ser acessada por qualquer um, é interessante que esteja em inglês para permitir que todos entendam;
Use os ícones propostos: estes ícones tem por objetivo imbuir de elementos gráficos as mensagens de commit, para trazer mais visibilidade e facilitar a coginição da mudança. Os ícones propostos estão na documentação, e devem ser utilizados para manter a padronização;
Reforço que a descrição do PR é o compilado das mensagens dos commits que compoem o PR;
Os PRs devem ser pequenos ou médios. Mesmo que esta medida seja subjetiva, é importante ter em vista que um PR atende a uma task ou issue, e que estas devem ser o mais granulares possíveis. Usando este princípio, os PRs consequentemente diminuem de tamanho. PRs grande número de linhas e arquivos modificados tornam-se extensos de serem revisados. Abaixo será inserido uma descrição de referencia de tamanhos de PR;
Caso seja incontornável a necessidade de fazer um PR grande, e mediante a apresentação de uma justificativa, a revisão deste deve ser feita de forma síncrona, em chamada envolvendo o autor e os revisores, para agilizar o processo;
PR's grandes sem justificativa devem ser rejeitados, para que sejam divididos pelo autor e facilitar assim o processo de Code Review;
Aprovação de sênior ou Tech Lead e contexto da atividade: Os PR's devem ser aprovados por, no mínimo, 2 avaliadores sendo 1 deles sênior ou líder técnico, e que este esteja no contexto da atividade desevolvida, para trazer clareza e entendimento à revisão;
Inserir o revisor principal como requerido: é interessante que, ao criar o PR, seja inserido o sênior ou TL que está no contexto da atividade como requerido. Isto evita a finalização do PR por revisores que não estejam no contexto da atividade desenvolvida;
Importância do refinamento técnico: para facilitar o processo de Code Review, é importante a divisão correta das tasks durante a cerimónia de refinamento técnico. Através destas, o desenvolvimento é dividido e assim, consequentemente, reduzido o tamanho dos PR's.
Estas orientações visam melhorar a qualidade das entregas dos nossos códigos, assim como agilizar o processo de Code Review, mantendo a cordialidade e bom clima no time. Neste contexto, para criação de comentários, orienta-se seguir as seguintes iniciativas:
Inserir razão do comentário: para trazer mais clareza à necessidade, descreva a razão deste. Desta forma o autor consegue identificar melhor a necessidade da mudança proposta;
Inclusão de exemplo: ao criar um comentário, busque inserir exemplo da mudança sugerida, se possível. Tal abordagem facilitará a correção por parte do autor;
Revise e comente independente da senioridade: todos podem revisar e criar comentários em PR'S. Além da melhoria do código, também é um momento de troca de experiencia. Mesmo um júnior revisão codigo de um sênior, deve fazer comentários caso achei necessário. Lembrando sempre de manter em vista o tato e a cordialidade.
Os pontos a seguir descrevem uma referência para avaliação do tamanho dos PRs:
Pequeno:
Alterações simples e de baixo impacto.
Poucas linhas de código adicionadas ou modificadas.
Alterações que não afetam diretamente outros componentes do sistema.
Implementação de pequenos ajustes ou correções de bugs.
Implementação de pequenas melhorias de desempenho.
Médio:
Alterações que envolvem a adição ou modificação de várias partes de um componente ou módulo.
Introdução de novos recursos ou funcionalidades que não são complexos.
Alterações que podem afetar indiretamente outros componentes, mas não exigem grandes alterações nesses componentes.
Implementação de melhorias que requerem um pouco mais de esforço de desenvolvimento e revisão.
Grande:
Alterações que envolvem a refatoração extensiva de um componente ou módulo.
Introdução de novos recursos ou funcionalidades complexas que exigem um grande esforço de desenvolvimento e revisão.
Alterações que têm um impacto significativo em vários componentes do sistema.
Alterações que exigem uma revisão detalhada de arquitetura e design.
Implementação de grandes melhorias de desempenho ou otimização.
Reforço que este processo é de melhoria contínua. Qualquer sugestão que tiverem será devidamente apreciada e incorporada aos processos caso seja relevante.
No mais, mais uma vez, obrigado pela atenção de todos.
 heart 7

	
            Azure DevOps Services | Sign In
        

