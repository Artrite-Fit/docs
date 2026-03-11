# Branch Model

## GitHub Flow

O GitHub Flow é um modelo de fluxo de trabalho (workflow) para o desenvolvimento de software utilizando o sistema de controle de versão Git e a plataforma GitHub.

Esse modelo organiza o desenvolvimento por meio do uso de **branches temporárias**, **Pull Requests** e **revisões de código**, permitindo que equipes trabalhem de forma colaborativa e organizada.

Os princípios-chave do GitHub Flow são apresentados a seguir.

---

## Princípios do GitHub Flow

### Branches

Cada nova funcionalidade, correção de bug ou tarefa é desenvolvida em uma branch separada. Essa prática permite que várias pessoas trabalhem em diferentes partes do projeto simultaneamente, sem interferir diretamente no trabalho umas das outras.

### Commits frequentes

Os desenvolvedores são encorajados a realizar commits frequentes em suas branches locais durante o desenvolvimento de uma funcionalidade ou correção. Essa prática contribui para a manutenção de um histórico detalhado do progresso e permite que outros membros da equipe acompanhem as mudanças em andamento.

### Pull Requests

Quando uma funcionalidade ou correção é concluída em uma branch, é aberto um **Pull Request (PR)** para mesclar as alterações na branch principal do repositório.

O Pull Request permite iniciar uma discussão com outros membros da equipe, revisar o código e fornecer feedback antes da integração das alterações na branch principal.

### Revisões de código

Os membros da equipe podem revisar o código enviado por meio dos Pull Requests. Durante esse processo, podem ser feitos comentários, solicitadas alterações ou realizada a aprovação do Pull Request.

A revisão de código é uma etapa importante para garantir a qualidade do software e promover o compartilhamento de conhecimento entre os membros da equipe.

---

# Tomada de decisão

O GitHub Flow foi escolhido como modelo de fluxo de trabalho devido à sua simplicidade, clareza e eficiência no desenvolvimento colaborativo.

Sua estrutura é fácil de compreender e adotar, pois não exige processos complexos ou múltiplas branches permanentes. Além disso, sua flexibilidade permite que equipes trabalhem em paralelo, desenvolvendo funcionalidades independentes em branches separadas, o que facilita a colaboração e reduz conflitos de código.

Outro fator importante é a colaboração proporcionada pelo uso de Pull Requests. Por meio desse mecanismo, os desenvolvedores podem compartilhar suas alterações, receber feedback e aprimorar a qualidade do código antes de integrá-lo à branch principal.

Além disso, o GitHub Flow fornece rastreabilidade e um histórico detalhado de cada funcionalidade ou correção desenvolvida em branches separadas. Isso facilita o acompanhamento do progresso do projeto, a identificação de alterações e a possibilidade de reverter mudanças quando necessário.

Por fim, o modelo também favorece a implantação contínua das alterações assim que elas são concluídas e mescladas na branch principal, acelerando a entrega de novas funcionalidades e correções.

---

# Estrutura de branches

O projeto utiliza uma única branch principal chamada **`main`**, que contém a versão estável do código.

Todas as novas funcionalidades, correções de bugs ou melhorias são desenvolvidas em **branches temporárias** criadas a partir da branch `main`.

Após o desenvolvimento e revisão do código, essas branches são mescladas novamente na branch principal.

---

# Como usar

Qualquer alteração presente na branch principal (`main`) deve estar estável e pronta para implantação. Antes de iniciar uma nova tarefa, recomenda-se verificar se existem **issues abertas** e priorizar as atividades a serem implementadas.

## Criação de uma nova ramificação

Para adicionar uma nova funcionalidade ao projeto, cria-se uma nova ramificação a partir da ramificação principal (`main`).

O nome da ramificação deve representar claramente a funcionalidade ou tarefa que está sendo desenvolvida.

Exemplos de nomenclatura incluem:

- `exercicio-beecrowd-####` (em que #### representa o número da questão do Beecrowd)
- `trabalho-nomeDoTrabalho`

## Implementação das alterações

Na nova ramificação são realizadas as alterações necessárias no código, como a implementação de funcionalidades ou a resolução de exercícios.

Durante essa etapa, é importante realizar testes para garantir que as alterações funcionem corretamente e não introduzam problemas no projeto.

Recomenda-se a realização de **commits frequentes e descritivos**, organizando o desenvolvimento em pequenas alterações lógicas.

## Abertura de Pull Request

Após a conclusão das alterações, deve-se abrir um **Pull Request** para que o código seja revisado e posteriormente integrado à ramificação principal.

O Pull Request permite que outros membros da equipe analisem o código, discutam possíveis melhorias e identifiquem eventuais problemas.

Além disso, o Pull Request também pode ser utilizado como ferramenta de colaboração quando há dificuldades na implementação de alguma funcionalidade. Nesse caso, o código desenvolvido até o momento pode ser compartilhado para que outros membros da equipe contribuam com sugestões ou soluções.

## Revisão do Pull Request

Durante o processo de Pull Request, os membros da equipe podem revisar as alterações propostas, fornecer comentários e sugerir melhorias.

As alterações podem ser discutidas e ajustadas até que estejam adequadas para integração ao projeto.

## Mesclagem do Pull Request

Após a aprovação do Pull Request e a conclusão das revisões necessárias, realiza-se a mesclagem das alterações na ramificação principal (`main`).

Esse processo integra as alterações à versão principal do projeto.

---

# Ciclo de vida de uma branch

Uma branch normalmente segue o seguinte ciclo de vida:

1. Criação da branch a partir da `main`
2. Desenvolvimento da funcionalidade ou correção
3. Abertura de Pull Request
4. Revisão de código
5. Mesclagem na `main`
6. Exclusão da branch após a integração

---

# Exclusão de branches

Após a mesclagem de um Pull Request, recomenda-se excluir a branch utilizada para o desenvolvimento. Essa prática ajuda a manter o repositório organizado e evita o acúmulo de branches antigas que não estão mais em uso.
