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
- **escopo**: parte do projeto que está sendo modificada (ex: `registro`, `auth`, `perfil`). Opcional.
- **assunto**: descrição breve do que foi realizado.
- **corpo** *(opcional)*: explicação mais detalhada das mudanças realizadas.
- **rodapé** *(opcional)*: informações adicionais, como referências a issues ou outras mudanças relacionadas.

---

# Tipos

Os tipos de mensagens de commit devem ser apenas um dentre os seguintes:

| Tipo | Descrição |
|-----|-----|
| **feat** | nova funcionalidade adicionada ao projeto |
| **fix** | correção de bug |
| **refactor** | alteração de código que não corrige um bug nem adiciona funcionalidade, mas melhora a estrutura ou organização |
| **docs** | alterações na documentação |
| **revert** | reversão de um commit anterior |
| **test** | adição ou correção de testes |
| **style** | alterações que não afetam o comportamento do código (formatação, espaços, etc.) |
| **perf** | melhoria de desempenho |
| **build** | alterações que afetam o sistema de compilação ou dependências externas |
| **chore** | mudanças de manutenção que não afetam diretamente o código fonte ou testes |
| **ci** | alterações relacionadas à configuração de integração contínua |
| **conflict** | resolução de conflitos de merge |

---

# Escopo

O escopo é opcional e indica qual parte do sistema está sendo modificada.

Alguns exemplos de escopos utilizados neste projeto incluem:

- `registro`
- `progresso`
- `biblioteca`
- `metas`
- `descobertas`
- `auth`
- `perfil`
- `notificacoes`
- `db`
- `api`

---

# Assunto

O assunto deve ser uma descrição clara e objetiva da alteração realizada.

Boas práticas:

- escrever em **letras minúsculas**
- utilizar **verbo no infinitivo**
- não utilizar **ponto final**

Exemplo:

```
feat(registro): adicionar suporte a atividades domésticas
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
feat(registro): adicionar suporte a atividades domésticas

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

```
feat(registro): adicionar suporte a atividades domésticas

fix(auth): corrigir expiração de token

docs(readme): atualizar instruções de instalação

refactor(progresso): reorganizar lógica de cálculo semanal

test(registro): adicionar testes para registro de atividade

ci: adicionar develop ao trigger de pull_request
```

---

# Exemplos de commits inválidos

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
feat(progresso): adicionar histórico semanal de atividades

gera relatório com as atividades físicas e domésticas
registradas pelo usuário durante a semana.

fixes #15
```
