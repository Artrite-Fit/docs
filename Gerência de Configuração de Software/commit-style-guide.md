# Guia de estilo para mensagens de commit

Este documento define o padrão de escrita das mensagens de commit utilizadas no projeto. O objetivo é manter o histórico de alterações claro, organizado e fácil de entender.

---

# Formato

As mensagens de commit devem seguir o seguinte formato:

```
[tipo](escopo): assunto

[corpo]

[rodapé]
```

Onde:

- **tipo**: palavra que descreve a natureza da mudança (ex: `feat`, `fix`, `docs`).
- **escopo**: parte do projeto que está sendo modificada (ex: `registro`, `atividades`, `interface`, `notificacoes`).
- **assunto**: descrição breve do que foi realizado.
- **corpo** *(opcional)*: explicação mais detalhada das mudanças realizadas.
- **rodapé** *(opcional)*: informações adicionais, como referências a issues ou outras mudanças relacionadas.

---

# Tipos

Os tipos de mensagens de commit devem ser apenas um dentre os seguintes:

| Tipo | Descrição |
|-----|-----|
| **FEAT** | nova funcionalidade adicionada ao projeto |
| **FIX** | correção de bug |
| **REFACTOR** | alteração de código que não corrige um bug nem adiciona funcionalidade, mas melhora a estrutura ou organização |
| **DOCS** | alterações na documentação |
| **REVERT** | reversão de um commit anterior |
| **TEST** | adição ou correção de testes |
| **STYLE** | alterações que não afetam o comportamento do código (formatação, espaços, etc.) |
| **PERF** | melhoria de desempenho |
| **BUILD** | alterações que afetam o sistema de compilação ou dependências externas |
| **CHORE** | mudanças de manutenção que não afetam diretamente o código fonte ou testes |
| **CI** | alterações relacionadas à configuração de integração contínua |
| **TYPO** | correção ortográfica em comentários ou documentação |
| **FUNC** | criação de função unitária no código |
| **IN** | adição de arquivos de entrada utilizados para popular o sistema |
| **UPDATE** | atualização de arquivo ou documento existente |
| **CONFLICT** | resolução de conflitos de merge |

---

# Escopo

O escopo indica qual parte do sistema está sendo modificada.

Alguns exemplos de escopos utilizados neste projeto incluem:

- `registro`
- `atividades`
- `interface`
- `relatorios`
- `perfil`
- `notificacoes`
- `login`

---

# Assunto

O assunto deve ser uma descrição clara e objetiva da alteração realizada.

Boas práticas:

- escrever em **letras minúsculas**
- utilizar **verbo no infinitivo**
- não utilizar **ponto final**

Exemplo:

```
feat(atividades): adicionar registro de caminhada
```

---

# Corpo

O corpo é opcional e pode ser utilizado para fornecer mais detalhes sobre a alteração realizada.

Ele pode incluir:

- explicação da mudança
- justificativa da alteração
- informações adicionais importantes

O corpo deve ser separado do assunto por **uma linha em branco**.

Exemplo:

```
feat(registro): permitir registrar atividades domésticas

adiciona opção para registrar atividades como cozinhar,
limpar a casa e cuidar do jardim.
```

---

# Rodapé

O rodapé também é opcional e pode conter informações adicionais, como:

- referências a issues
- identificação de tarefas concluídas
- relação com outros commits

O rodapé deve ser separado do corpo por **uma linha em branco**.

Exemplo:

```
fix(registro): corrigir erro no salvamento das atividades

corrige falha que impedia o registro correto das atividades
domésticas realizadas pelo usuário.

fixes #27
```

---

# Regras gerais

Para manter o histórico do projeto organizado, recomenda-se seguir as seguintes boas práticas:

- cada commit deve representar **uma única alteração lógica**
- as mensagens devem ser **claras e objetivas**
- evitar commits muito grandes que misturem diferentes alterações
- sempre utilizar o tipo apropriado para descrever a mudança
- verificar se o sistema está funcionando corretamente antes de realizar o commit

---

# Exemplos de commits válidos

Alguns exemplos de commits seguindo o padrão definido:

```
feat(atividades): adicionar registro de caminhada

feat(registro): permitir registrar atividades domésticas

fix(registro): corrigir erro no salvamento de atividades

docs(readme): atualizar instruções de instalação

refactor(atividades): reorganizar lógica de registro de atividades

test(registro): adicionar testes para registro de atividades
```

---

# Exemplos de commits inválidos

Os exemplos abaixo **não seguem o padrão definido**:

```
atualizações
arrumei bugs
mudanças no sistema
commit
```

Problemas nesses commits:

- não possuem tipo definido
- não indicam escopo
- não descrevem claramente a alteração realizada

---

# Exemplo completo

```
feat(relatorios): adicionar histórico semanal de atividades

gera relatório com as atividades físicas e domésticas
registradas pelo usuário durante a semana.

fixes #15
```
