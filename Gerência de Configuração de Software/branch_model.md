# Branch Model

## GitHub Flow com branch de integração

O Vivasso adota uma variação do GitHub Flow, acrescida de uma branch de integração (`develop`) que serve como camada de validação antes que o código chegue à `main`.

---

## Princípios do GitHub Flow

### Branches

Cada nova funcionalidade, correção de bug ou tarefa é desenvolvida em uma branch separada. Essa prática permite que várias pessoas trabalhem em diferentes partes do projeto simultaneamente, sem interferir diretamente no trabalho umas das outras.

### Commits frequentes

Os desenvolvedores são encorajados a realizar commits frequentes em suas branches locais durante o desenvolvimento de uma funcionalidade ou correção. Essa prática contribui para a manutenção de um histórico detalhado do progresso e permite que outros membros da equipe acompanhem as mudanças em andamento.

### Pull Requests

Quando uma funcionalidade ou correção é concluída em uma branch, é aberto um **Pull Request (PR)** para mesclar as alterações na branch de destino.

O Pull Request permite iniciar uma discussão com outros membros da equipe, revisar o código e fornecer feedback antes da integração das alterações.

### Revisões de código

Os membros da equipe podem revisar o código enviado por meio dos Pull Requests. Durante esse processo, podem ser feitos comentários, solicitadas alterações ou realizada a aprovação do Pull Request.

A revisão de código é uma etapa importante para garantir a qualidade do software e promover o compartilhamento de conhecimento entre os membros da equipe.

---

# Tomada de decisão

O GitHub Flow foi escolhido como modelo de fluxo de trabalho devido à sua simplicidade, clareza e eficiência no desenvolvimento colaborativo.

A adição da branch `develop` foi motivada pela necessidade de uma camada de integração entre as branches temporárias e a `main`. Como o projeto possui múltiplas frentes em desenvolvimento paralelo, ter um ponto de convergência antes da versão estável reduz o risco de integração e permite que o código seja validado em conjunto antes de ser considerado pronto para implantação.

---

# Estrutura de branches

| Branch | Papel |
|---|---|
| `main` | Versão estável. Código aqui está pronto para implantação. |
| `develop` | Branch de integração. Features chegam aqui primeiro e são validadas antes de subir para a `main`. |
| `feat/<descricao>` | Nova funcionalidade. Criada a partir da `develop`. |
| `fix/<descricao>` | Correção de bug. Criada a partir da `develop`. |
| `hotfix/<descricao>` | Correção crítica em produção. Criada a partir da `main` e mergeada de volta na `main` e na `develop`. |

A descrição deve usar apenas letras minúsculas e hífens para separar palavras.

**Exemplos:**
- `feat/registro-de-atividade`
- `fix/calculo-progresso-semanal`
- `hotfix/crash-ao-salvar-meta`

---

# Fluxo de trabalho

O fluxo normal de desenvolvimento segue o caminho:

**`feat/` ou `fix/`** → PR para `develop` → CI passa → merge → PR para `main` → merge

O `hotfix/` é a única exceção: parte da `main` e retorna direto para ela, sendo depois sincronizado com a `develop`.

---

# Como usar

Qualquer alteração presente na branch principal (`main`) deve estar estável e pronta para implantação. Antes de iniciar uma nova tarefa, recomenda-se verificar se existem **issues abertas** e priorizar as atividades a serem implementadas.

## Criação de uma nova ramificação

Para adicionar uma nova funcionalidade ao projeto, cria-se uma nova ramificação a partir da `develop`.

O nome da ramificação deve seguir o formato `<tipo>/<descricao>`, representando claramente a natureza e o objetivo da tarefa.

## Implementação das alterações

Na nova ramificação são realizadas as alterações necessárias no código. Recomenda-se a realização de **commits frequentes e descritivos**, organizando o desenvolvimento em pequenas alterações lógicas e seguindo o padrão definido no guia de commits.

## Abertura de Pull Request

Após a conclusão das alterações, deve-se abrir um **Pull Request** com destino à `develop`. O título do PR deve descrever claramente o propósito das alterações realizadas.

O Pull Request também pode ser utilizado como ferramenta de colaboração quando há dificuldades na implementação de alguma funcionalidade. Nesse caso, o código desenvolvido até o momento pode ser compartilhado para que outros membros da equipe contribuam com sugestões ou soluções.

## CI e revisão

O CI roda automaticamente ao abrir o PR, verificando lint, build e type check. Enquanto o CI não passar, o merge não deve ser realizado.

Após o CI verde, o autor deve verificar o checklist de PR antes de realizar o merge.

## Checklist de PR

O CI cobre lint, build e type check automaticamente. Antes do merge, verificar apenas o que o CI não cobre:

- [ ] A descrição do PR está clara e explica o que foi feito
- [ ] A branch está atualizada com a `develop`
- [ ] Nenhuma credencial, chave de API ou dado sensível foi incluído no commit
- [ ] As mensagens de commit seguem o padrão definido

## Mesclagem do Pull Request

Após o CI passar e o checklist ser verificado, realiza-se a mesclagem das alterações na branch de destino.

---

# Ciclo de vida de uma branch

Uma branch normalmente segue o seguinte ciclo de vida:

1. Criação da branch a partir da `develop` (ou `main`, no caso de `hotfix/`)
2. Desenvolvimento da funcionalidade ou correção
3. Abertura de Pull Request
4. CI passa
5. Revisão pelo checklist
6. Mesclagem na branch de destino
7. Exclusão da branch após a integração

---

# Exclusão de branches

Após a mesclagem de um Pull Request, recomenda-se excluir a branch utilizada para o desenvolvimento. Essa prática ajuda a manter o repositório organizado e evita o acúmulo de branches antigas que não estão mais em uso.
