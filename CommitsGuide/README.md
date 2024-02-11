⬅️[Voltar para página inicial]()

# Introdução

Esse documento tem por objetivo normalizar os commits do fluxo de GIT, seguindo o padrão proposto [pela convenção de commits](https://www.conventionalcommits.org/), que procura padronizar os commits a fim de seguirem o versionamento semântico proposto pelo [SemVer](https://semver.org).
Logo, há uma ligação quase um para um entre o tipo de commit e a mudança da versão do software.

O importante de notar aqui é que a padronização das mensagens de commit não apenas ajuda na automação do processo de versionamento como também, se bem implementada, descreve o Changelog completo do software quase automaticamente.
___

[Introdução](#introdução)

[Padrão/Cheatsheet](#padrãocheatsheet)

[Especificação](#especificação)

[Tipos de commit](#TiposdeCommit)

[Exemplos](#exemplos)

[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)
[Introdução](#introdução)

___

# Padrão/Cheatsheet

**Padrão**
```
<emoji | tipo>[escopo adicional - OPCIONAL]: <descrição>

[corpo de texto - OPCIONAL]

[rodapé com links para o DevOps - OPCIONAL]
```

**Exemplo**
```
✨feat: Add an awesome new feature
```

- Para casos que necessitam de maior nível de detalhe, é possível efetuar como o exemplo a seguir:
**Exemplo**
```
✨feat(api/core): Add an awesome new feature

This is an example of a commit's body.
- Add a new item to list
- Add even another item to list

Relates #1234
```

> 💡 **Mensagens em Inglês**

> 💡 **Mensagens devem ser declarativas e sintetizadas!**
>
>> ❌ **Não Faça:** `New endpoint was added to send data to new componente XYZ in the front end, resolving task #123` 
>>
>> ✅ **Faça:** `Add endpoint GET to component XYZ`


## Tipos de commit:

```
📦build
🔧chore
♾️ci
📚docs
✨feat
🐞fix
⚡perf
♻refactor
↩revert
🎨style
🎯test
🚧wip
```
___

# Especificação

A especificação oficial do padrão proposto pela conveção pode ser encontrado [aqui](https://www.conventionalcommits.org/).

A seguir, enumeraremos o padrão proposto pelo time Quality do Nexus, baseado na convenção oficial.

> 💡 As palavras chave utilizadas na especificação devem ser interpretadas de acordo com a resolução [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt)

1. Commits DEVEM ser prefixados com um tipo e seu emoji correspondente, seguidos de escopo OPCIONAL, entre parênteses, e ponto de exclamação caso se trate de uma BREAKING CHANGE; e REQUER ser seguido por dois pontos e um espaço.

**Exemplo**
```
✨feat: add new endpoint to create QualityGateController
❗✨feat: remove QualityGate creator in GET QualityGate
✨feat (api\QualityGateController): add new endpoint to create QualityGateController
```

2. O tipo ✨feat DEVE adicionar novas funcionalidades à aplicação.
3. O tipo 🐞fix DEVE corrigir um bug/issue/erro na aplicação.
4. Um Escopo PODE ser adicionado após o tipo e DEVE ser um ou mais substantivos descrevendo uma parte ou domínio do sistema, entre parênteses. 

**Exemplo**
```✨feat (api\QualityGateController): ...```

5. Uma descrição DEVE seguir imediatamente após o tipo/escopo, os dois pontos e o espaço em branco. A descrição é um breve sumário das mudanças realizadas.
6. Uma descrição mais longa do commit PODE ser adicionada no corpo do commit, após a descrição, provendo informações adicionais sobre o contexto das mudanças realizadas. DEVE existir uma linha em branco entre o cabeçalho do commit e o seu corpo.
7. O corpo do commit tem formato livre e PODE possuir qualquer número de parágrafos separados por quebras de linha.
8. Um ou mais rodapés PODEM ser adicionados, e DEVEM vir após o corpo do commit, separado de uma linha em branco. Cada rodapé DEVE consistir de uma palavra chave, seguindo o padrão `:<espaço>` ou `<espaço>#` (inspirado pela [conveção do GIT Trailer](https://git-scm.com/docs/git-interpret-trailers)).

**Exemplo** `Fixes: Bug 12345 - bug description` | `Fixes #12345, #6789`.

9. As plavras chave do rodapé DEVEM ser separadas por hífens `-`, para melhor separar a visualização entre o rodapé e demais parágrafos do corpo do commit.

**Exemplo** `Reviewed-by: Z` | `Approved-by: X` | `Acked-by: Y`.
   - ⚠ EXCEÇÃO: Breaking Changes devem ser sempre serem adicionadas na forma: `❗ BREAKING CHANGES:`.
10. O valor de cada rodapé PODE conter espaços e quebras de linha e DEVE terminar quando um novo rodapé válido (palavra chave + separador) for observado.
11. BREACKING CHANGES DEVEM ser indicadas pela presença de um emoji `❗` antes do emoji relativo ao tipo e de um ponto de exclamação após o par tipo/escopo (exemplo: `❗✨feat: remove QualityGate creator in GET QualityGate` ), e DEVEM também possuir um rodapé explicando as mudanças que geram a quebra de código.
12. Todas as unidades de informação do commit NÃO DEVEM ser case sensitive, por implementação, a exceção de BREAKING CHANGES que DEVEM ser sempre UPPER CASE.

**Observação**
Este guia basea-se na convensão de committs, e por isto apresenta os casos acima descritos. Salvo excessões, DEVE-SE utilizar o padrão apresentado até o item 5.

___

# Tipos de Commit

## 1. 🐞 fix

Corrige um problema no sistema. Correlacionado ao versionamento [PATCH](http://semver.org/#summary) no Versionamento Semântico.

## 2. ✨ feat

Adiciona uma nova funcionalidade no sistema. Correlacionado ao versionamento [MINOR](http://semver.org/#summary) no Versionamento Semântico.

## 3. ⚡ perf

Mudança visando otimizar a performance do sistema. Correlacionado ao versionamento [MINOR](http://semver.org/#summary) no Versionamento Semântico não oficialmente. 

**Exemplo**
Melhora de uma query; alteração da forma de renderização para otimizar o carregamento de uma tela; adicionar lazy loading; mudar o contrato de retorno da API para reduzir o tráfego de rede; etc

___

## 🔖 Outros tipos suportados

Desmais tipos de commit tem por objetivo tornar mais fácil a compreensão das mudanças efetuadas no código.

### 4. 📦 build

Mudanças que afetam o processo de build do sistema, como adição de bibliotecas e dependências, mudanças de versão, etc.

**Exemplo** 
adicionar/remover/atualizar npm; mudanças no NUGET;

### 5. 🔧 chore

Mudanças de qualidade de vida de código. Não afetam o sistema em si, mas a qualidade de desenvolvimento. Isso pode ocorrer via a adição de linter, prettier, ferramentas de automação, etc.

**Exemplo** 
Mudança nas regras de lint; adicionar prettier; adicionar mais extensões de arquivos ao .gitignore; adicionar swagger; adicionar storybook; etc

### 6. ♾️ ci

Mudanças relacionada ao fluxo de Continuos Integration (CI).

**Exemplo**
Mudança no YAML da pipeline.

### 7. 📚 docs

Adiciona documentação à base de código.

**Exemplo** 
Documentação de uma função; documentação do inner source; mudanças no README do projeto; 

### 8. ♻ refactor

Manutenção na base de código que não gera mudança de comportamento do sistema. 

**Exemplo**
Reescrita de uma parte do código para melhorar a leitura; aplicar uma mudança solicitada em code review; 

### 9. ↩ revert

Reverte uma mudança no sistema.

**Exemplo**
Commit revertendo o sistema para uma versão anterior

### 10. 🎨 style

Mudanças de ESTILO DE CÓDIGO que não geram nenhuma mudança no sistema (como adicionar ou apagar espaços e linhas em branco, quebras de linha). São aplicados em geral por regras de LINTER ou Prettier de código automaticamente, ou mudança no padrão de nomenclatura do time, etc.

**Exemplo**
Mudar o style-guide; mudar de convenção lint e aplicar no código; arrumar indentações; remover espaços em brancos; remover comentários; 

### 11. 🎯 test

Criação ou mudança de códigos de teste.

**Exemplo**
Criação de testes unitários, de integração; 

### 12. 🚧 WIP

Código em progresso. Deve ser utilizado em casos de uma implementação não finalizada.

### 13. 🌐 Intl

Mudanças de internacionalização e localização, como adição de suporte para uma nova linguagem, ou mudanças nos dicionários já existentes.

# Foo

**Exemplo**
Mudança nos registros de localização de uma lingua; criação de um novo dicionário de tradução; exclusão de registros não mais utilizados; 

___

## ❗ BREAKING CHANGE

Breaking Chances são mudanças relacionadas ao versionamento [MAJOR](http://semver.org/#summary) no Versionamento Semântico. Diferentemente dos tipos, uma BREAKING CHANGE é um modificador adicionado ao tipo do commit. Deve ser utilizado sempre que uma mudança que gerar incompatibilidade com uma versão anterior, seja qualquer a origem desta.

É composto por:

- Emoji `❗` antes do emoji padrão do tipo;
- Demais orientações para preenchimento da mensagem de commit

**Exemplo**

```
❗✨feat(api/user)!: Change GET user endpoint return contract
```
___

## Escopos
 
Escopos são informações contextuais adicionais que acompanham o tipo de mudança realizada no código. Pode ser entendido como a parte do negócio, domínio ou entidade bem definida da solução. Isso pode incluir o fluxo de login, uma entidade importante como Usuário, ou mesmo um processo como uma requisição.
O escopo pode ser especificado quando a mudança for mais especifica dentro de uma grande entidade, deixando mais transparente a modificação. Por exemplo, se houver uma grande mudança dentro do processo de uma requisição, mais especificamente na parte de autenticação, pode ser interessante adicionar como escopo `(request/auth)`. Pode descrever também qual aplicação foi modificada dentro do contexto, como: front-end ou UI (User Interface), back-end ou api, microservice XPTO. 

Os escopos são sempre adicionados entre parênteses logo após o tipo da mudança, antes do dois pontos.

Essa informação contextual pode ser utilizada para futuramente localizar todas as mudanças realizadas para aquele escopo dentro do Changelog, ou mesmo filtrar todo o histórico de commits.
___
# Exemplos

1. Completo ( título + corpo + rodapé )

```
🐞fix(log): Fix log mapping

Shows the log levels: "info", "warn", "error" e "critical".

Relates #12345
```

2. Apenas título

```
✨feat: Add feature XYZ
```

3. Título + Descrição

```
♻refactor(log): Improve application log management

- Add log levels enum
- Normalize log functions
- Add log configuration
```

4. Título + rodapé

```
🐞fix(login): Fix user login flow

Relates #12345
```
___

# Referências

- [Conveção](https://www.conventionalcommits.org/)
- https://www.linkapi.solutions/blog/conventional-commits-pattern
- [Commit Lint - GITHub](https://github.com/conventional-changelog/commitlint)
- https://nitayneeman.com/posts/understanding-semantic-commit-messages-using-git-and-angular/
- [Padrão RFC 2119 - PT/BR](https://webiwg.github.io/rfc-pt/rfc2119)
- [Padrão RFC 2119](https://www.ietf.org/rfc/rfc2119.txt)
