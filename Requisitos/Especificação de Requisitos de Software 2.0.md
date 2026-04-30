# Especificação de Requisitos de Software

[1\. Introdução](#1.-introdução)

[2\. Classes de usuários](#2.-classes-de-usuários)

[3\. Definição de conceitos](#3.-definição-de-conceitos)

[4\. Requisitos de Software](#4.-requisitos-de-software)

[4.1. Requisitos funcionais](#4.1.-requisitos-funcionais)

[Cadastro](#cadastro)

[Login](#login)

[Triagem](#triagem)

[IPAQ (Questionário Internacional de Atividade Física \- Forma Curta)](#ipaq-\(questionário-internacional-de-atividade-física---forma-curta\))

[eHEALS (Escala de Letramento Digital em Saúde)](#eheals-\(escala-de-letramento-digital-em-saúde\))

[PAM-13 (Patient Activation Measure)](#pam-13-\(patient-activation-measure\))

[Registro de Atividades](#registro-de-atividades)

[Metas](#metas)

[Lembretes](#lembretes)

[Progresso](#progresso)

[FACIT-F](#facit-f)

[Aprender / Descobertas](#aprender-/-descobertas)

[Gamificação](#gamificação)

[Portal do administrador (Parte Web)](#portal-do-administrador-\(parte-web\))

[Feedback](#feedback)

[Smartphone Usability questionnaiRE (SURE)](#smartphone-usability-questionnaire-\(sure\))

[User Version of the Mobile App Rating Scale (uMARS)](#user-version-of-the-mobile-app-rating-scale-\(umars\))

[Suitability Assessment of Materials (SAM)](#suitability-assessment-of-materials-\(sam\))

[4.2. Requisitos não-funcionais](#4.2.-requisitos-não-funcionais)

[Acessibilidade](#acessibilidade)

[Disponibilidade](#disponibilidade)

[Requisitos de Produto](#requisitos-de-produto)

[Segurança/Privacidade](#segurança/privacidade)

[5\. Rastreabilidade de requisitos](#5.-rastreabilidade-de-requisitos)

[6\. Histórico de Versões](#6.-histórico-de-versões)

# 

# 1\. Introdução {#1.-introdução}

Este documento registra os requisitos detalhados do sistema Vivasso, descrevendo as funcionalidades e características esperadas do produto na forma de requisitos textuais.

O Vivasso é uma plataforma de monitoramento de saúde e atividade física voltada ao acompanhamento do bem-estar e da evolução física dos seus pacientes. Inicialmente direcionado a pessoas que convivem com doenças reumáticas, o sistema busca apoiar o registro de atividades físicas, atividades do cotidiano e indicadores relacionados à saúde, como níveis de dor e fadiga. Diferentemente de aplicativos de fitness voltados exclusivamente para desempenho atlético, o Vivasso prioriza o bem-estar integral e o acompanhamento seguro da atividade física.

O ecossistema do aplicativo é estruturado em uma jornada que vai do acolhimento inicial à análise de dados do paciente. Durante o processo de onboarding, o utilizador responde questionários validados cientificamente, como IPAQ e FACIT-F, que ajudam a estabelecer uma linha de base para sua condição de saúde. A partir desse momento, o sistema permite o registro de atividades físicas e esforços cotidianos, que são convertidos em equivalentes metabólicos (MET), possibilitando o acompanhamento do progresso semanal do paciente.

Além do monitoramento de atividades, o Vivasso também atua como uma plataforma de informação e incentivo à adoção de hábitos saudáveis. Por meio da seção Descobertas, o aplicativo disponibiliza conteúdos educativos e sugestões de exercícios físicos adaptados às necessidades dos pacientes. Ao longo do uso, o sistema gera relatórios de evolução que relacionam atividade física, metas estabelecidas e níveis de dor registrados, permitindo ao paciente acompanhar sua própria evolução e possibilitando análises agregadas que podem apoiar profissionais de saúde ou pesquisadores no entendimento da adesão a práticas saudáveis.

# 2\. Classes de usuários {#2.-classes-de-usuários}

| Classes de usuários | Descrição |
| :---- | :---- |
| Paciente | Usuário principal do sistema. Pessoa que utiliza o aplicativo para registrar atividades físicas e domésticas, informar níveis de dor, acompanhar metas, visualizar progresso e acessar conteúdos educativos sobre atividades físicas. |
| Administrador | Gestor da plataforma responsável pela curadoria de conteúdos educativos, gestão da base de dados e análise de métricas agregadas de utilização e adesão ao sistema. Também acompanha relatórios gerados pela plataforma para apoiar estudos, melhorias do aplicativo e monitoramento geral do uso. |
| Administrador\_Mestre | Herda Administrador, possibilita gerenciar Administradores |

# 3\. Definição de conceitos {#3.-definição-de-conceitos}

Nesta seção são descritos os principais conceitos relevantes para o domínio do sistema.

| Nome do Conceito | Definição |
| :---- | :---- |
| MET | Unidade utilizada para estimar o gasto energético de atividades físicas. |
| EVA | Escala visual analógica numérica utilizada para registrar a intensidade da dor percebida pelo usuário, variando de 0 (ausência de dor) a 10 (dor máxima). |
| IPAQ (International Physical Activity Questionnaire | Questionário internacional utilizado para avaliar o nível de atividade física de um indivíduo. |
| FACIT-F (Functional Assessment of Chronic Illness Therapy – Fatigue) | Instrumento utilizado para medir o nível de fadiga em pacientes com doenças crônicas. |
| Onboarding | Processo de integração do usuário ao aplicativo, no qual são apresentados os objetivos e funcionalidades do sistema. |
| Triagem | Processo inicial onde o usuário responde questionários para avaliar a saúde. |
| Gamificação | Estratégia utilizada pelo sistema para incentivar o engajamento do usuário por meio de recompensas digitais, como medalhas ou conquistas ao atingir determinadas metas. |
| Dashboard | Tela do aplicativo onde o usuário pode visualizar informações resumidas sobre seu progresso, metas e atividades registradas. |

# 

# 4\. Requisitos de Software {#4.-requisitos-de-software}

Nesta seção são descritos os requisitos textuais do produto. Na Seção 4.1 são descritos os requisitos funcionais. Na Seção 4.2 são descritos os requisitos não-funcionais.

## 4.1. Requisitos funcionais {#4.1.-requisitos-funcionais}

### **Cadastro** {#cadastro}

1. O sistema deve permitir que o usuário realize cadastro com a conta google ou cadastro tradicional, inserindo os campos individualmente.

2. O sistema deve validar o preenchimento obrigatório do campo nome completo no cadastro do paciente.

3. O sistema deve restringir a entrada do campo nome completo apenas a caracteres alfabéticos e espaços em branco.

4. O sistema deve validar o preenchimento obrigatório do campo e-mail no cadastro do paciente.

5. O sistema deve validar o formato do campo e-mail de acordo com o padrão de endereçamento da RFC 5322\.

6. O sistema deve validar o preenchimento obrigatório do campo nome de usuário no cadastro.

7. O sistema deve restringir o campo nome de usuário ao uso de caracteres alfanuméricos minúsculos, pontos e sublinhados, sendo obrigatório o início por um caractere alfabético.

8. O sistema deve validar o preenchimento obrigatório do campo telefone no cadastro do paciente.

9. O sistema deve restringir a entrada do campo telefone a valores numéricos que incluam o Código de Endereçamento Postal (DDD) e o número da linha.

10. O sistema deve validar o preenchimento obrigatório do campo de nascimento no cadastro do paciente.

11. O sistema deve restringir a entrada do campo de nascimento a datas iguais ou anteriores à data atual do servidor.

12. O sistema deve validar o preenchimento do campo sexo no registro do paciente e deve restringir a seleção às opções Masculino, Feminino, Intersexo e Não Informado.

13. O sistema deve validar o preenchimento obrigatório do campo nível de escolaridade no cadastro do paciente.

14. O sistema deve restringir a seleção do campo nível de escolaridade às opções: Analfabeto, Fundamental Incompleto, Fundamental Completo, Médio Incompleto, Médio Completo, Superior Incompleto, Superior Completo e Pós Graduação.

15. O sistema deve validar o preenchimento obrigatório do campo cor ou raça no cadastro do paciente.

16. O sistema deve restringir a seleção do campo cor ou raça às opções definidas pelo Instituto Brasileiro de Geografia e Estatística: Branca, Preta, Amarela, Parda, Indígena.

17. O sistema deve validar o preenchimento obrigatório do campo estado civil no cadastro do paciente.

18. O sistema deve restringir a seleção do campo estado civil às opções definidas pelo Código Civil Brasileiro: Solteiro, Casado, Divorciado, Viúvo e Separado Judicialmente.

19. O sistema deve registrar o tipo de artrite do paciente como um campo obrigatório.

20. O sistema deve restringir a seleção do campo do tipo de artrite às opções: 

21. O sistema deve registrar o tempo de tratamento do paciente e o tempo de diagnóstico como um campos opcionais.

22. O sistema deve registrar o tempo de tratamento do paciente com limite inferior “Menos de um ano” e sem limite superior.

23. O sistema deve registrar o tempo de diagnóstico do paciente com limite inferior “Menos de um ano” e sem limite superior.

24. O sistema deve permitir a criação de senhas compostas por caracteres alfanuméricos.

25. O sistema deve fornecer a possibilidade de autenticação do paciente por meio do provedor de identidade Google.

26. O sistema deve registrar a aceitação dos termos da Lei Geral de Proteção de Dados (LGPD) pelo paciente.

27. O sistema deve registrar o consentimento do paciente para o processamento de dados de saúde.

28. O sistema, durante o cadastro, deve validar a autenticação do paciente, a partir de um envio no email cadastrado.

29. O sistema deve apresentar as perguntas de triagem ao paciente durante o cadastro.

    ### **Login** {#login}

1. O sistema deve autenticar o acesso do usuário mediante o fornecimento de nome de usuário e senha.

2. O sistema deve autenticar o acesso do usuário mediante o fornecimento de e-mail e senha.

3. O sistema deve mascarar os caracteres inseridos no campo de senha durante a digitação.

4. O sistema deve exibir uma mensagem de erro em caso de falha na autenticação, sem especificar qual campo (usuário ou senha) está incorreto.

5. O sistema deve suportar o preenchimento automático de credenciais através do gerenciador de senhas nativo do sistema operacional.

6. O sistema deve permitir a autenticação do usuário por meio de integração com o serviço Google Identity.

7. O sistema deve disponibilizar funcionalidade de redefinição de senha através do envio de um link de recuperação para o e-mail cadastrado.

8. O sistema deve permitir tentativas de login ilimitadas para o usuário.

9. O sistema deve disponibilizar a opção de persistência da sessão de autenticação do paciente entre acessos à aplicação.

   ### **Triagem** {#triagem}

1. O sistema deve redirecionar obrigatoriamente o paciente para a tela de triagem após o primeiro login bem-sucedido no aplicativo mobile.

2. O sistema deve exibir uma tela introdutória informando que a triagem é composta por três etapas obrigatórias: Questionário Internacional de Atividade Física (IPAQ \- forma curta), eHEALS e Patient Activation Measure 13 (PAM-13).

3. O sistema deve salvar o progresso da triagem de forma persistente entre as etapas do IPAQ, eHEALS e PAM-13, permitindo a retomada em caso de fechamento do aplicativo.

   #### ***IPAQ (Questionário Internacional de Atividade Física \- Forma Curta)*** {#ipaq-(questionário-internacional-de-atividade-física---forma-curta)}

4. O sistema deve registar se o paciente possui trabalho remunerado através das opções Sim ou Não.

5. O sistema deve registar a quantidade de horas que o paciente trabalha por dia através de um campo numérico.

6. O sistema deve registar os anos de estudo completos do paciente através de um campo numérico.

7. O sistema deve registar a autopercepção de saúde geral do paciente através das opções: Excelente, Muito boa, Boa, Regular ou Ruim.

8. O sistema deve apresentar as instruções obrigatórias do IPAQ antes do início da coleta, enfatizando o foco em atividades de uma semana normal, a inclusão de atividades em diversos contextos (trabalho, lazer, casa) e a regra mínima de 10 minutos contínuos por atividade.

9. O sistema deve apresentar visualmente as definições de Atividades Vigorosas (esforço grande e respiração muito forte) e Atividades Moderadas (algum esforço e respiração um pouco mais forte).

10. O sistema deve registar a frequência semanal (0 a 7 dias ou opção "Nenhum") e o tempo gasto por dia (horas e minutos) para atividades físicas vigorosas.

11. O sistema deve registar a frequência semanal (0 a 7 dias ou opção "Nenhum") e o tempo gasto por dia (horas e minutos) para atividades físicas moderadas, exibindo um aviso para não incluir caminhada nesta contagem.

12. O sistema deve registar a frequência semanal (0 a 7 dias ou opção "Nenhum") e o tempo gasto por dia (horas e minutos) para caminhadas realizadas por pelo menos 10 minutos contínuos.

13. O sistema deve registar o tempo gasto sentado (horas e minutos) num dia de semana e num dia de final de semana.

14. O sistema deve impedir o avanço no formulário IPAQ caso o campo de dias seja superior a 7 ou o campo de minutos seja superior a 59\.

15. O sistema deve desabilitar os campos de tempo do IPAQ caso a opção "Nenhum" seja selecionada para os dias da semana da respetiva atividade.

16. O sistema deve permitir o progresso para o eHEALS apenas após a conclusão e validação de todas as respostas do IPAQ.

    #### ***eHEALS (Escala de Letramento Digital em Saúde)*** {#eheals-(escala-de-letramento-digital-em-saúde)}

17. O sistema deve apresentar o texto introdutório do eHEALS, esclarecendo que o termo "recursos de saúde" engloba páginas da internet e aplicativos.

18. O sistema deve disponibilizar uma escala de resposta de 5 pontos (Discordo totalmente, Discordo em parte, Não tenho certeza, Concordo em parte, Concordo totalmente) para cada afirmação do eHEALS.

19. O sistema deve registar a resposta do paciente para as afirmações: "Eu sei quais recursos de saúde estão disponíveis na internet", "Eu sei onde encontrar recursos de saúde úteis na internet" e "Eu sei como encontrar recursos de saúde úteis na internet".

20. O sistema deve registar a resposta do paciente para as afirmações: "Eu sei como usar a internet para esclarecer minhas dúvidas sobre saúde" e "Eu sei como usar as informações sobre saúde que encontro na internet para me ajudar".

21. O sistema deve registar a resposta do paciente para as afirmações: "Eu tenho as habilidades de que preciso para avaliar os recursos de saúde que encontro na internet", "Eu consigo diferenciar os recursos de saúde que são de alta qualidade dos que são de baixa qualidade" e "Eu me sinto seguro ao usar informações da internet para tomar decisões relacionadas à saúde".

22. O sistema deve validar o preenchimento de todas as 8 afirmações do eHEALS antes de permitir o acesso ao PAM-13.

    #### ***PAM-13 (Patient Activation Measure)*** {#pam-13-(patient-activation-measure)}

23. O sistema deve apresentar o texto introdutório do PAM-13, reforçando que as respostas devem ser verdadeiras para o paciente e não o que se espera de um profissional de saúde.

24. O sistema deve disponibilizar uma escala de resposta de 4 pontos (Discordo totalmente, Discordo, Concordo, Concordo totalmente) e a opção "N/A \- Não se aplica" para cada frase do PAM-13.

25. O sistema deve registrar a resposta para a pergunta: "No final das contas, você é a pessoa responsável por cuidar de sua saúde?".

26. O sistema deve registrar a resposta para a pergunta: "A sua participação ativa no cuidado de sua saúde é a coisa mais importante que influencia sua saúde?".

27. O sistema deve registrar a resposta para a pergunta: "Você tem confiança de que pode ajudar a prevenir ou reduzir problemas ligados à sua saúde?".

28. O sistema deve registrar a resposta para a pergunta: "Você sabe para que serve cada um dos medicamentos que lhe foram prescritos?".

29. O sistema deve registrar a resposta para a pergunta: "Você tem confiança de que sabe quando precisa ir ao médico ou serviço de saúde ou se você mesmo(a) consegue cuidar de um problema de saúde?".

30. O sistema deve registrar a resposta para a pergunta: "Você tem confiança de que pode contar suas preocupações ao profissional da saúde mesmo quando ele não lhe pergunta?".

31. O sistema deve registrar a resposta para a pergunta: "Você tem confiança de que é capaz de seguir os tratamentos de saúde que você precisa fazer em sua casa?".

32. O sistema deve registrar a resposta para a pergunta: "Você entende os seus problemas de saúde e as causas desses problemas?".

33. O sistema deve registrar a resposta para a pergunta: "Você sabe quais são os tratamentos disponíveis para seus problemas de saúde?".

34. O sistema deve registrar a resposta para a pergunta: "Você tem conseguido manter as mudanças no estilo de vida, como se alimentar corretamente ou fazer exercícios?".

35. O sistema deve registrar a resposta para a pergunta: "Você sabe como prevenir problemas com sua saúde?".

36. O sistema deve registrar a resposta para a pergunta: "Você tem confiança de que consegue encontrar soluções quando surgem novos problemas com sua saúde?".

37. O sistema deve registrar a resposta para a pergunta: "Você tem confiança de que consegue manter as mudanças no estilo de vida, como se alimentar corretamente e fazer exercícios, mesmo em períodos de estresse (situações desfavoráveis)?".

38. O sistema deve validar o preenchimento de todas as 13 afirmações do PAM-13 antes de finalizar a triagem e liberar o acesso para tela inicial.

    ### **Registro de Atividades** {#registro-de-atividades}

1. O sistema deve permitir que o paciente registre as atividades realizadas, com a opção de escolher atividades pré-cadastradas, com base no [Compêndio de Atividades](https://docs.google.com/document/d/1u2988vsKRR8RPz-eJ5vb5nLICPNTiezKhnXuW4rnPvE/edit?tab=t.0).

2. O sistema deve permitir que o paciente selecione a intensidade do exercício entre leve, moderado e intenso.

3. O sistema deve permitir que o paciente selecione a duração da atividade em horas (de 0 a 24), minutos (0 a 59\) e segundos (0 a 59), com duração mínima de 5 minutos e máxima de 24 horas.

4. O sistema deve permitir que o paciente selecione o nível de dor de 0 a 10, permitindo apenas números inteiros.

5. O sistema deve salvar o Resultado em MET multiplicado pelo número de minutos.

6. O sistema deve somar os minutos ao progresso diário e semanal.

7. O sistema deve somar o MET ao progresso diário e semanal.

8. O sistema deve permitir visualizar os registros anteriores.

9. O sistema deve permitir que o paciente altere/exclua um registro de atividade durante 3 dias após ser gerado.

   ### 	**Metas** {#metas}

1. O sistema deve permitir que o paciente registre uma meta semanal de atividades em minutos.

2. O sistema deve, semanalmente, utilizar a meta semanal anterior como default para a semana atual. 

3. O sistema deve restringir a definição de metas personalizadas ao valor mínimo de 1 minuto.

4. O sistema deve permitir o registro de metas personalizadas sem estipular um valor máximo de minutos.

5. O sistema deve aplicar o valor padrão de 150 minutos para a meta semanal na ausência de uma definição customizada pelo paciente.

6. O sistema deve restringir o registro de uma meta personalizada igual a padrão (150 minutos).

7. O sistema deve exibir o histórico das metas semanais das semanas anteriores para consulta do paciente.

8. O sistema deve permitir que o paciente “reative” uma meta semanal antiga.

9. O sistema deve exibir a meta da semana vigente para acompanhamento do paciente.

10. O sistema deve permitir que o paciente desabilite o recebimento de notificações push relacionadas às metas.

11. O sistema deve enviar uma notificação push quando o paciente atingir a meta semanal estabelecida.

12. O sistema deve apresentar o progresso percentual da meta semanal na tela principal do aplicativo.

13. O sistema deve permitir que o paciente desative as notificações externas das metas estabelecidas.

    ### **Lembretes** {#lembretes}

1. O sistema deve permitir o cadastro de lembretes personalizados compostos por um título obrigatório e uma mensagem de texto opcional.

2. O sistema deve permitir que o paciente selecione os dias da semana para a recorrência de cada lembrete.

3. O sistema deve permitir a seleção dos dias da semana e horários para o disparo das notificações de lembrete.

4. O sistema deve restringir que um paciente adicione dois lembretes personalizados no mesmo dia e horário.

5. O sistema deve permitir a configuração do horário de disparo para cada lembrete cadastrado.

6. O sistema deve emitir alertas de lembrete exclusivamente por meio de notificações do sistema operacional.

7. O sistema deve permitir que o paciente desative as notificações externas das metas estabelecidas.

8. O sistema deve configurar, de forma predefinida, um lembrete de incentivo e registro de atividades para disparar diariamente às 08:00.

9. O sistema deve configurar, de forma predefinida, um lembrete de registro de atividades para disparar diariamente às 20:00.

10. O sistema deve permitir a edição, ativação e desativação de lembretes personalizados pelo paciente.

11. O sistema deve permitir a ativação e desativação dos lembretes padrões da aplicação pelo paciente.

12. O sistema deve disparar notificações automáticas de lembrete de registro após identificar 1, 3, 7, 15 e 30 dias consecutivos de inatividade do usuário.

    ### 	**Progresso** {#progresso}

1. No último dia da semana, o sistema deve solicitar que o paciente preencha o questionário do [FACIT-F](#facit-f) para poder visualizar seu progresso semanal

2. O sistema deve exibir, na tela inicial, um gráfico de progresso circular indicando a razão entre os minutos de atividades realizadas e a meta estabelecida.

3. O sistema deve exibir a quantidade de atividade realizada em MET (Equivalente Metabólico) através de um gráfico circular.

4.  O sistema deve exibir um texto descritivo posicionado adjacente ao gráfico de progresso com o formato "X de Y minutos completados".

5. O sistema deve exibir a evolução da atividade física em minutos através de gráficos de barras simples.

6. O sistema deve exibir a evolução do nível de dor, em uma escala de 0 a 10, através de gráficos de barras simples.

7. O sistema deve disponibilizar filtros para visualização dos gráficos em escala semanal.

8. O sistema deve disponibilizar filtros para visualização dos gráficos em escala mensal.

9. O sistema deve disponibilizar filtros para visualização dos gráficos em escala anual.

10. O sistema deve permitir que o paciente gere um relatório semanal consolidado dos dados do paciente.

11. O sistema deve persistir os registros de atividade física e nível de dor para histórico do paciente.

12. O sistema deve exportar o relatório de progresso no formato PDF.

13.  O sistema deve permitir o compartilhamento do resultado por e-mail.

14. O sistema deve permitir o compartilhamento do resultado por aplicativos de mensagens instantâneas.

    #### ***FACIT-F*** {#facit-f}

15. O sistema deve permitir que o usuário acesse o formulário de Escala de Fadiga FACIT-F (Versão 4\) através da seção de Registro de Atividades.

16. O sistema deve exibir obrigatoriamente a instrução: "Faça um círculo ou marque um número por linha para indicar a sua resposta no que se refere aos últimos 7 dias."

17. O sistema deve disponibilizar para cada pergunta uma escala Likert de 5 pontos: 0 (Nem um pouco), 1 (Um pouco), 2 (Mais ou menos), 3 (Muito) e 4 (Muitíssimo).

18. O formulário deve conter a pergunta (H17): "Sinto-me fatigado/a."

19. O formulário deve conter a pergunta (HI12): "Sinto fraqueza generalizada."

20. O formulário deve conter a pergunta (An1): "Sinto-me sem forças (sem vontade para nada)."

21. O formulário deve conter a pergunta (An2): "Sinto-me cansado/a."

22. O formulário deve conter a pergunta (An3): "Tenho dificuldade em começar as coisas porque estou cansado/a."

23. O formulário deve conter a pergunta (An4): "Tenho dificuldade em acabar as coisas porque estou cansado/a."

24. O formulário deve conter a pergunta (An5): "Tenho energia."

25. O formulário deve conter a pergunta (An7): "Sou capaz de fazer as minhas atividades habituais."

26. O formulário deve conter a pergunta (An8): "Preciso (de) dormir durante o dia."

27. O formulário deve conter a pergunta (An12): "Estou cansado/a demais para comer."

28. O formulário deve conter a pergunta (An14): "Preciso de ajuda para fazer as minhas atividades habituais."

29. O formulário deve conter a pergunta (An15): "Estou frustrado/a por estar cansado/a demais para fazer as coisas que quero."

30. O formulário deve conter a pergunta (An16): "Tenho que limitar as minhas atividades sociais por estar cansado/a."

31. O sistema deve validar se todos os 13 itens foram respondidos antes de permitir o envio do formulário.

    ### **Aprender / Descobertas** {#aprender-/-descobertas}

1. O sistema deve disponibilizar uma biblioteca de conteúdos educativos composta por textos (com formatação rica), vídeos (incorporados ou via link) e infográficos.

2. O sistema deve organizar a biblioteca nas seguintes categorias obrigatórias: Artrite Reumatoide; Artrite Psoriásica; Espondiloartrite; Benefícios da Atividade Física; Tipos de Atividade Física; Dicas para Dias com Dor.

3. O sistema deve permitir que o utilizador realize pesquisas textuais na biblioteca para encontrar conteúdos específicos por palavras-chave.

4. O sistema deve permitir que o utilizador "favorite" (marque como preferido) artigos ou vídeos para acesso rápido numa secção dedicada de "Favoritos".

5. O sistema deve exibir um marcador visual (ex: "Lido" ou "Visto") nos conteúdos que o utilizador já consumiu integralmente.

6. O sistema deve permitir a partilha de conteúdos da biblioteca através de links externos para aplicações de mensagens ou e-mail.

7. O sistema deve permitir o download de conteúdos textuais e imagens para visualização offline (RNF relacionado: Disponibilidade).

8. O sistema deve apresentar uma área de "Destaques" com os conteúdos mais recentes publicados pelo administrador.

9. O sistema deve apresentar sugestões de leitura baseadas no tipo de artrite selecionado no perfil, sem bloquear o acesso às restantes categorias.

10. O sistema deve disponibilizar uma funcionalidade de "Conteúdo Aleatório" ou "Sugestão do Dia" para incentivar a exploração de temas diversos da biblioteca.

11. O sistema deve exibir o tempo estimado de leitura ou duração do vídeo na pré-visualização do conteúdo na seção Descobertas.

12. O sistema deve permitir que o utilizador avalie o conteúdo (ex: "Útil" ou "Não Útil") para fornecer feedback indireto ao administrador sobre a qualidade do material.

    ### **Gamificação** {#gamificação}

1. O sistema deve atribuir títulos ao paciente com base nos critérios de pontuação definidos no [Documento do Sistema de Conquistas](https://docs.google.com/document/d/11b9PzDt-7W-LTD7LMumk-6NDkSFN2ZoT_iRxFWh3s0U/edit?tab=t.0).

2. O sistema deve exibir visualmente o nível atual do paciente na interface do perfil de usuário.

3. O sistema deve manter as funcionalidades e o fluxo de navegação inalterados, independentemente do nível ou título alcançado pelo paciente.

4. O sistema deve atualizar o título do paciente em tempo real assim que os critérios de conquista forem atingidos.

   ### **Portal do administrador (Parte Web)** {#portal-do-administrador-(parte-web)}

1. O sistema deve autenticar o administrador mediante fornecimento de e-mail (ou usuário) e senha exclusivos.

2. O sistema deve listar os dados dos pacientes em formato tabular, permitindo ordenação e filtragem (ex: por nome, diagnóstico ou data de cadastro).

3. O sistema deve gerar dashboards e gráficos para visualização agregada dos dados dos pacientes (ex: distribuição de diagnósticos, níveis de atividade).

4. O sistema deve permitir que o administrador desative o acesso ao aplicativo móvel de forma global, impedindo novas sincronizações ou acessos até que seja reativado.

5. O sistema deve oferecer uma interface para criação e edição de artigos ou avisos que serão exibidos na seção informativa do aplicativo móvel.

6. O sistema deve permitir a inclusão, edição e exclusão de opções no campo "Diagnóstico" exibido no cadastro do paciente.

7. O sistema deve permitir a criação e manutenção de um catálogo de tipos de artrite para classificação clínica no sistema.

8. O sistema deve permitir o gerenciamento (CRUD) de atividades físicas, contendo: Nome, Categoria e Nível de Gasto MET por Nível de Intensidade Física.

9. O sistema deve permitir a criação de categorias personalizadas para organizar as atividades.

10. O sistema deve permitir a alteração de qualquer atributo das atividades (nome, categoria, MET) a qualquer momento, com propagação das mudanças para o aplicativo móvel.

11. O sistema deve permitir ao administrador marcar um conteúdo como "Destaque" para que apareça prioritariamente na seção Descobertas.

12. O sistema deve permitir ao administrador visualizar métricas de visualização e avaliação (Útil/Não Útil) de cada conteúdo da biblioteca.

13. O Sistema deve permitir que o Administrador\_Mestre possa gerenciar outros administradores.

    ### **Feedback** {#feedback}

    #### ***Smartphone Usability questionnaiRE (SURE)*** {#smartphone-usability-questionnaire-(sure)}

1. O sistema deve permitir que o usuário responda a cada pergunta utilizando uma escala Likert de 5 pontos, sendo: 0 (Não se aplica \- N/A), 1 (Discordo), 2 (Discordo), 3 (Concordo) e 4 (Concordo totalmente).

2. O sistema deve exibir a pergunta: "Eu achei fácil inserir dados nestes aplicativos. Por exemplo, utilizando código QR, listas de opções etc.", e guardar a resposta do paciente.

3. O sistema deve exibir a pergunta: "Quando eu cometo um erro é fácil de corrigi-lo.", e guardar a resposta do paciente.

4. O sistema deve exibir a pergunta: "Eu achei que a ajuda/dica dada pelo aplicativo foi útil.", e guardar a resposta do paciente.

5. O sistema deve exibir a pergunta: "Foi fácil encontrar as informações que precisei.", e guardar a resposta do paciente.

6. O sistema deve exibir a pergunta: "Eu me senti no comando usando este aplicativo.", e guardar a resposta do paciente.

7. O sistema deve exibir a pergunta: "Eu achei adequado o tempo que levei para completar as tarefas.", e guardar a resposta do paciente.

8. O sistema deve exibir a pergunta: "Foi fácil de aprender a usar este aplicativo.", e guardar a resposta do paciente.

9. O sistema deve exibir a pergunta: "A sequência das ações no aplicativo corresponde à maneira como eu normalmente as executo. Por exemplo, a ordem de botões, campo de dados, etc.", e guardar a resposta do paciente.

10. O sistema deve exibir a pergunta: "É fácil fazer o que eu quero usando este aplicativo.", e guardar a resposta do paciente.

11. O sistema deve exibir a pergunta: "Foi fácil navegar nos menus e telas do aplicativo.", e guardar a resposta do paciente.

12. O sistema deve exibir a pergunta: "O aplicativo atende às minhas necessidades.", e guardar a resposta do paciente.

13. O sistema deve exibir a pergunta: "Eu recomendaria este aplicativo para outras pessoas.", e guardar a resposta do paciente.

14. O sistema deve exibir a pergunta: "Mesmo com pressa eu conseguiria executar as tarefas nesse aplicativo.", e guardar a resposta do paciente.

15. O sistema deve exibir a pergunta: "Eu achei o aplicativo consistente. Por exemplo, todas as funções podem ser realizadas de uma maneira semelhante.", e guardar a resposta do paciente.

16. O sistema deve exibir a pergunta: "É fácil lembrar como fazer as coisas neste aplicativo.", e guardar a resposta do paciente.

17. O sistema deve exibir a pergunta: "Eu usaria este aplicativo com frequência.", e guardar a resposta do paciente.

18. O sistema deve exibir a pergunta: "A organização dos menus e comandos de ação (como botões e links) é lógica, permitindo encontra-los facilmente na tela.", e guardar a resposta do paciente.

19. O sistema deve exibir a pergunta: "Eu consegui completar as tarefas com sucesso usando este aplicativo.", e guardar a resposta do paciente.

20. O sistema deve exibir a pergunta: "Eu gostei de usar este aplicativo.", e guardar a resposta do paciente.

21. O sistema deve exibir a pergunta: "O aplicativo fornece todas as informações necessárias para completar as tarefas de forma clara e compreensível.", e guardar a resposta do paciente.

22. O sistema deve exibir a pergunta: "Eu achei o aplicativo muito complicado de usar.", e guardar a resposta do paciente.

23. O sistema deve exibir a pergunta: "Os símbolos e ícones são claros e intuitivos.", e guardar a resposta do paciente.

24. O sistema deve exibir a pergunta: "Eu achei os textos fáceis de ler.", e guardar a resposta do paciente.

25. O sistema deve exibir a pergunta: "Eu achei o aplicativo desnecessariamente complexo. Precisei lembrar, pesquisar ou pensar muito para completar as tarefas.", e guardar a resposta do paciente.

26. O sistema deve exibir a pergunta: "A terminologia utilizada nos textos, rótulos, títulos etc. é fácil de entender.", e guardar a resposta do paciente.

27. O sistema deve exibir a pergunta: "Eu precisaria de apoio de uma pessoa para usar este aplicativo.", e guardar a resposta do paciente.

28. O sistema deve exibir a pergunta: "Eu me senti confortável usando este aplicativo.", e guardar a resposta do paciente.

29. O sistema deve exibir a pergunta: "O aplicativo se comportou como eu esperava.", e guardar a resposta do paciente.

30. O sistema deve exibir a pergunta: "Eu achei frustrante usar este aplicativo.", e guardar a resposta do paciente.

31. O sistema deve exibir a pergunta: "Eu achei que as várias funções do aplicativo são bem integradas.", e guardar a resposta do paciente.

32. O sistema deve exibir a pergunta: "Eu me senti muito confiante usando este aplicativo.", e guardar a resposta do paciente.

33. O sistema deve somar a pontuação desse formulário.

    #### ***User Version of the Mobile App Rating Scale (uMARS)*** {#user-version-of-the-mobile-app-rating-scale-(umars)}

34. O sistema deve apresentar a pergunta: "Interesse: O aplicativo é interessante de usar? Ele apresenta suas informações de maneira interessante em comparação com outros aplicativos semelhantes?". Respostas: 1\) Nada interessante. 2\) Desinteressante em grande parte. 3\) OK, nem interessante nem desinteressante; envolveria o usuário por um breve período (\< 5 minutos). 4\) Moderadamente interessante; envolveria o usuário por algum tempo (5-10 minutos no total). 5\) Muito interessante, envolveria o usuário no uso constante.

35. O sistema deve apresentar a pergunta: "Entretenimento: O aplicativo é divertido/interessante de usar? Possui componente que o tornam mais divertido do que outros aplicativos semelhantes?". Respostas: 1\) Chato, nada divertido ou interessante. 2\) Entediante em grande parte. 3\) OK, divertido o suficiente para entreter o usuário por um breve período (\< 5 minutos). 4\) Moderadamente divertido e interessante, iria entreter o usuário por algum tempo (5-10 minutos no total). 5\) Altamente interessante e divertido, estimularia o uso repetido. 6\) N/A Não se aplica para esse aplicativo.

36. O sistema deve apresentar a pergunta: "Customização: Ele permite que você personalize as configurações e preferências que você gostaria (por exemplo, som, conteúdo e notificações)?". Respostas: 1\) Não permite qualquer personalização ou requer que a configuração seja inserida todas às vezes. 2\) Permite pouca personalização e isso limita as funções do app. 3\) Personalização básica para funcionar adequadamente. 4\) Permite inúmeras opções de personalização. 5\) Permite a personalização completa das características/preferências do usuário, lembra todas as configurações.

37. O sistema deve apresentar a pergunta: "Interatividade: Ele permite a entrada do usuário, fornece feedback, contém prompts (lembretes, opções de compartilhamento, notificações etc.)?". Respostas: 1\) Sem recursos interativos e/ou sem resposta à entrada do usuário. 2\) Alguns recursos interativos, mas não suficientes, que limitam as funções do aplicativo. 3\) Recursos interativos básicos para funcionar adequadamente. 4\) Oferece uma variedade de recursos interativos, feedback e opções de entrada do usuário. 5\) Nível muito alto de capacidade de resposta por meio de recursos interativos, feedback e opções de entrada do usuário.

38. O sistema deve apresentar a pergunta: "Grupo alvo: O conteúdo do aplicativo (visual, linguagem, design) é apropriado para o público-alvo?". Respostas: 1\) Completamente inadequado, pouco claro ou confuso. 2\) Parcialmente inapropriado, pouco claro ou confuso. 3\) Aceitável, mas não especificamente projetado para o público-alvo. Pode ser impróprio/obscuro/confuso às vezes. 4\) Projetado para o público-alvo, com pequenos problemas. 5\) Projetado especificamente para o público-alvo, nenhum problema encontrado.

39. O sistema deve apresentar a pergunta: "Atuação: Com que precisão/rápido os recursos do aplicativo (funções) e componentes (botões/menus) funcionam?". Respostas: 1\) Aplicativo está quebrado; nenhuma/insuficiente/resposta imprecisa (por exemplo, falhas/bugs/recursos quebrados, etc.). 2\) Algumas funções funcionam, mas estão atrasadas ou contêm grandes problemas técnicos. 3\) App funciona no geral. Alguns problemas técnicos precisam ser corrigidos ou são lentos às vezes. 4\) Em grande parte funcional com problemas menores/insignificantes. 5\) Totalmente funcional, nenhum bug técnico encontrado.

40. O sistema deve apresentar a pergunta: "Fácil de usar: Quão fácil é aprender a usar o aplicativo; quão claras são as abas de menus, ícones e instruções?". Respostas: 1\) Sem/instruções limitadas; abas de menus, ícones são confusos; complicados. 2\) Leva muito tempo ou esforço. 3\) Leva algum tempo ou esforço. 4\) Fácil de aprender (ou tem instruções claras). 5\) Capaz de usar o aplicativo imediatamente; intuitivo; simples (sem instruções necessárias).

41. O sistema deve apresentar a pergunta: "Navegação: A movimentação entre as telas faz sentido; O aplicativo tem todos os links necessários entre as telas?". Respostas: 1\) Nenhuma conexão lógica entre as telas/a navegação é difícil. 2\) Compreensível após muito tempo/esforço. 3\) Compreensível após algum tempo/esforço. 4\) Fácil de entender/navegar. 5\) Fluxo de tela perfeitamente lógico, fácil, claro e intuitivo por toda parte e/ou possui atalhos.

42. O sistema deve apresentar a pergunta: "Design gestual: Os toques / batidas / apertos / rolagem fazem sentido? Eles são consistentes em todos os componentes/telas?". Respostas: 1\) Completamente inconsistente/confuso. 2\) Muitas vezes inconsistente/confuso. 3\) OK, com algumas inconsistências/elementos confusos. 4\) Principalmente consistente/intuitivo com problemas insignificantes. 5\) Perfeitamente consistente e intuitivo.

43. O sistema deve apresentar a pergunta: "Layout: A disposição e o tamanho dos botões, ícones, menus e conteúdo na tela são apropriados?". Respostas: 1\) Design muito ruim, confuso, algumas opções impossíveis de selecionar, localizar, ver ou ler. 2\) Design ruim, aleatório, pouco claro, algumas opções difíceis de selecionar/localizar/ver/ler. 3\) Satisfatório, poucos problemas para selecionar/localizar/ver/ler itens. 4\) Em grande parte claro, capaz de selecionar/localizar/ver/ler itens. 5\) Profissional, simples, claro, ordenado, logicamente organizado.

44. O sistema deve apresentar a pergunta: "Gráficos: Qual é a qualidade/resolução dos elementos gráficos usados para botões, ícones, menus e conteúdo?". Respostas: 1\) Parecem amadores, design visual muito ruim \- desproporcional estilisticamente inconsistente. 2\) De baixa qualidade/baixa resolução; design visual de baixa qualidade – desproporcional. 3\) De qualidade moderada e design visual (geralmente consistentes em estilo). 4\) Elementos gráficos e design visual de alta qualidade/resolução – principalmente proporcionais consistentes em estilo. 5\) Elementos gráficos e design visual de alta qualidade/resolução \- proporcionais consistentes em estilo por toda parte. 6\) N/A Não há informações dentro do aplicativo.

45. O sistema deve apresentar a pergunta: "Apelo visual: Quão bom é o aplicativo?". Respostas: 1\) Feio, desagradável de se ver, mal projetado, conflitante, cores incompatíveis. 2\) Ruim – mal projetado, mau uso de cores, visualmente chato. 3\) OK – mediano, nem agradável, nem desagradável. 4\) Agradável – gráficos perfeitos – consistente e projetados profissionalmente. 5\) Bonito – muito atraente, memorável, se destaca; o uso de cores aprimora os recursos/menus do aplicativo.

46. O sistema deve apresentar a pergunta: "Qualidade da informação: O conteúdo do aplicativo está correto, bem escrito e relevante para o objetivo/tópico do aplicativo?". Respostas: 1\) Irrelevante/inadequado/incoerente/incorreto. 2\) Pobre. Pouco relevante/apropriado/coerente/pode estar incorreto. 3\) Moderadamente relevante/apropriado/coerente/e parece correto. 4\) Relevante/adequado/coerente/correto. 5\) Altamente relevante, apropriado, coerente e correto. 6\) N/A Não há informações no aplicativo.

47. O sistema deve apresentar a pergunta: "Quantidade de informações: As informações no aplicativo são completas e objetivas?". Respostas: 1\) Mínima ou com muita informação. 2\) Insuficiente ou possivelmente completas e objetivas. 3\) As informações são OK. 4\) Oferece uma ampla gama de informações, possui algumas lacunas ou detalhes desnecessários; ou não tem links para mais informações e recursos. 5\) As informações são completas e objetivas; contêm links para mais informações e recursos. 6\) N/A Não há informações no aplicativo.

48. O sistema deve apresentar a pergunta: "Informações visuais: A explicação visual dos conceitos – através de tabelas/gráficos/imagens/vídeos, etc. – é clara, lógica, correta?". Respostas: 1\) Nada claro/confuso/errado ou necessário, mas ausente. 2\) Geralmente pouco claro/confuso/errado. 3\) Aceitável, porém às vezes pouco claro/confuso/errado. 4\) Em grande parte claro/lógico/correto. 5\) Perfeitamente claro/lógico/correto. 6\) N/A Não há informações visuais no aplicativo (por exemplo, contém apenas áudio ou texto).

49. O sistema deve apresentar a pergunta: "Credibilidade da fonte: as informações dentro do aplicativo parecem vir de uma fonte confiável?". Respostas: 1\) Fonte suspeita. 2\) Falta credibilidade. 3\) Não é suspeito, mas a legitimidade da fonte não é clara. 4\) Possivelmente vem de uma fonte legítima. 5\) Definitivamente vem de uma fonte legítima/especializada. 6\) N/A Não há informações no aplicativo.

50. O sistema deve apresentar a pergunta: "Você recomendaria este aplicativo para pessoas que possam se beneficiar dele?". Respostas: 1\) Não recomendo este aplicativo a ninguém. 2\) Há muito poucas pessoas para quem eu recomendaria este aplicativo. 3\) Talvez existam várias pessoas para quem eu recomendaria este aplicativo. 4\) Há muitas pessoas para quem eu recomendaria este aplicativo. 5\) Definitivamente eu recomendaria este aplicativo a todos.

51. O sistema deve apresentar a pergunta: "Quantas vezes você acha que usaria este aplicativo nos próximos 12 meses se fosse relevante para você?". Respostas: 1\) Nenhuma, pois talvez não seja necessário. 2\) 1-2 vezes, se necessário. 3\) 3-10 vezes, se necessário. 4\) 10-50 vezes. 5\) \>50 vezes.

52. O sistema deve apresentar a pergunta: "Você pagaria por este aplicativo?". Respostas: 1\) Definitivamente não. 2\) Acredito que não. 3\) Não sei. 4\) Acredito que sim. 5\) Definitivamente sim.

53. O sistema deve apresentar a pergunta: "Qual é a sua classificação geral (estrelas) do aplicativo?". Respostas: 1\) \* Um dos piores aplicativos que já usei. 2\) \*\*. 3\) \*\*\* Média. 4\) \*\*\*\*. 5\) \*\*\*\*\* Um dos melhores aplicativos que usei.

54. O sistema deve apresentar a pergunta: "Conscientização – Este aplicativo aumentou minha conscientização sobre a importância de abordar meus hábitos/comportamentos saudáveis.". Respostas: 1\) Discordo totalmente; 2\) Discordo em algumas coisas; 3\) Não concordo e nem discordo; 4\) Concordo em algumas coisas; 5\) Concordo totalmente.

55. O sistema deve apresentar a pergunta: "Conhecimento – Este aplicativo aumentou meu conhecimento/compreensão para meus hábitos/comportamentos saudáveis.". Respostas: 1\) Discordo totalmente; 2\) Discordo em algumas coisas; 3\) Não concordo e nem discordo; 4\) Concordo em algumas coisas; 5\) Concordo totalmente.

56. O sistema deve apresentar a pergunta: "Atitudes – O aplicativo mudou minhas atitudes para melhorar esses meus hábitos/comportamentos saudáveis.". Respostas: 1\) Discordo totalmente; 2\) Discordo em algumas coisas; 3\) Não concordo e nem discordo; 4\) Concordo em algumas coisas; 5\) Concordo totalmente.

57. O sistema deve apresentar a pergunta: "Intenção de mudar – O aplicativo aumentou minhas intenções/motivação para abordar hábitos/comportamentos saudáveis.". Respostas: 1\) Discordo totalmente; 2\) Discordo em algumas coisas; 3\) Não concordo e nem discordo; 4\) Concordo em algumas coisas; 5\) Concordo totalmente.

58. O sistema deve apresentar a pergunta: "Busca de ajuda – Este aplicativo me encorajaria a procurar mais ajuda para lidar com meus hábitos/comportamentos saudáveis (se eu precisar).". Respostas: 1\) Discordo totalmente; 2\) Discordo em algumas coisas; 3\) Não concordo e nem discordo; 4\) Concordo em algumas coisas; 5\) Concordo totalmente.

59. O sistema deve apresentar a pergunta: "Mudança de comportamento – O uso deste aplicativo aumentará/diminuirá meus hábitos/comportamentos saudáveis.". Respostas: 1\) Discordo totalmente; 2\) Discordo em algumas coisas; 3\) Não concordo e nem discordo; 4\) Concordo em algumas coisas; 5\) Concordo totalmente.

60. O sistema deve apresentar a pergunta: "Mais comentários sobre o aplicativo?". Respostas: Questão aberta discursiva.

61. O sistema deve somar a pontuação desse formulário.

    #### ***Suitability Assessment of Materials (SAM)*** {#suitability-assessment-of-materials-(sam)}

62. O sistema deve disponibilizar 3 campos fechados de múltipla escolha para cada pergunta: Ótimo (2) pontos, Adequado (1), Não Adequado (0), Não pode ser Avaliado (Deve-se guardar a quantidade de vezes que “Não pode ser Avaliado” foi escolhida).

63. O sistema deve apresentar as perguntas relacionadas a Conteúdo: (a) O propósito está evidente (b) O conteúdo trata de comportamentos (c) O conteúdo está focado no propósito (d) O conteúdo destaca os pontos principais. Então, o sistema deve salvar a pontuação de Conteúdo.

64. O sistema deve apresentar as perguntas relacionadas a Exigências de alfabetização: (a) Nível de leitura (b) Usa escrita na voz ativa (c) Usa vocabulário com palavras comuns no texto (d) O contexto vem antes de novas informações (e) O aprendizado é facilitado por tópicos. Então, o sistema deve salvar a pontuação de Exigências de alfabetização.

65. O sistema deve apresentar as perguntas relacionadas a Ilustrações: (a) O propósito da ilustração referente ao texto está adequado (b) Tipos de ilustração (c) As figuras/ilustrações são relevantes (d) As listas, tabelas, etc. tem explicação (e) As ilustrações tem legenda. Então, o sistema deve salvar a pontuação de Ilustrações.

66. O sistema deve apresentar as perguntas relacionadas a Layout e Apresentações: (a) Característica do layout (b) Tamanho e tipo de letra (c) São utilizados subtítulos. Então, o sistema deve salvar a pontuação de Layout e Apresentações.

67. O sistema deve apresentar as perguntas relacionadas a Estimulação/Motivação do aprendizado: (a) Utiliza a interação (b) As orientações são específicas e dão exemplos (c) Motivação e autoeficácia. Então, o sistema deve salvar a pontuação de Estimulação/Motivação do aprendizado.

68. O sistema deve apresentar as perguntas relacionadas a Adequação cultural: (a) É semelhante a sua lógica, linguagem e experiência (b) Imagem cultural e exemplos. Então, o sistema deve salvar a pontuação de Adequação cultural.

69. Por fim, os requisitos devem explicar a lógica de cálculo final do SAM: S \= Pontuação total SAM (todos os fatores (Exemplo: pontuação de Conteúdo \+ outras categorias)). M \= Pontuação máxima total \= 44\. N \= Número de respostas N/As acima multiplicado por 2\. T \= Pontuação máxima total ajustada \= (M-N). Percentual de pontuação \= S dividido por T (S/T). Interpretação da pontuação adequada: (70%–100% material superior, 40%–69% material adequado, 0%–39% material inadequado).

## 4.2. Requisitos não-funcionais {#4.2.-requisitos-não-funcionais}

### **Acessibilidade** {#acessibilidade}

1. O aplicativo deve ser construído levando em consideração as possíveis limitações causadas pelas artrites

   ### **Disponibilidade** {#disponibilidade}

2. O sistema deve permitir o funcionamento de notificações locais mesmo sem conexão com internet.

3. O sistema deve permitir o funcionamento de registros mesmo sem conexão com internet.

   ### **Requisitos de Produto** {#requisitos-de-produto}

4. O sistema deve funcionar, inicialmente, em dispositivos móveis Android, mas com possibilidade para IOS.

5. O sistema deve ser escrito em uma linguagem simples, motivadora e de fácil entendimento.

   ### **Segurança/Privacidade** {#segurança/privacidade}

6. O sistema deve prover mecanismos de proteção que garantam o armazenamento seguro e o acesso restrito aos dados de saúde, impedindo acessos não autorizados e garantindo a privacidade do usuário.

7. O sistema deve permitir um número ilimitado de tentativas de autenticação no login.

# 5\. Rastreabilidade de requisitos {#5.-rastreabilidade-de-requisitos}

A rastreabilidade bidirecional entre os requisitos aqui descritos e os demais artefatos do sistema está definida em [matriz\_rastreabilidade.xlsx](https://docs.google.com/spreadsheets/d/1QWvlw39eaN-fns38WfiKEWtzMmChCx6h/edit?usp=drive_web&ouid=114022228384079605796&rtpof=true). Todos elementos rastreados, incluindo os requisitos, utilizam seus identificadores únicos como referência no documento de rastreabilidade.

# 

# 6\. Histórico de Versões {#6.-histórico-de-versões}

| Versão | Data | Membros | Alterações |
| :---- | :---- | :---- | :---- |
| 0.0 | 11/03/2026 | Caio Tome | Criação Inicial do Documento |
| 0.1 | 12/03/2026 | Caio Tome, João Pedro Da Cruz, José Navarro, Lourdes Oshiro | Inclusão da introdução, classes de usuários, definição de conceitos, requisitos funcionais e não funcionais |
| 0.5 | 16/03/2026 | Caio Tome | Formatação, reorganização e reescrita para apresentação para validação com proponente |
| 0.6 | 17/03/2026 | Caio Tome | Reescrita do documento considerando a validação do proponente e as classes de usuários |
| 0.7 | 23/03/2026 | Caio Tome e José Navarro | Mudança no documento considerando as perguntas respondidas |
| 1.0 | 25/03/2026 | Caio Tome, João Pedro Da Cruz, José Navarro, Lourdes Oshiro | Definição 1.0 do documento após proponente responder as perguntas de ALTA prioridade |
| 1.1 | 30/03/2026 | Caio Tome e José Navarro |  |
| 1.2 | 31/03/2026 | José Navarro | Definição do sistema de gamificação |
| 1.3 | 01/04/2026 | Caio Tome e José Navarro | Melhoria na parte de Registro de atividades |
| 1.4 | 07/04/2026 | José Navarro | Melhoria módulos de autenticação (login e cadastro), metas e lembretes em requisitos funcionais |
| 1.5 | 09/04/2026 | Caio Tome | Finalização dos Requisitos de Triagem usando os artefatos que o proponente forneceu |
| 1.6 | 15/04/2026 | João Pedro | Refinamento nos requisitos de Aprender/Bilioteca, Descobertas e Portal do Administrador |
| 1.7 | 20/04/2026 | Caio Tome | Requisitos Levantados, Reescritos e movidos para uma nova seção, Feedback, cujo objetivo é avaliar a experiência do usuário usando os questionários fornecidos pelo proponente. |
| 1.8 | 22/04/2026 | Caio Tome | Adição do Último questionário solicitado pelo proponente em Requisitos \> FACIT-F |
| 1.81 | 23/04/2026 | Caio Tome | FACIT-F transferido para Progresso |
| 1.9 | 27/04/2026 | Caio Tome | Melhoria no registro de Aprender/Biblioteca de Conteúdo e Descobertas e Portal do Administrador |
| 2.0 | 30/04/2026 | Caio Tome | Mudança na forma de identificação dos requisitos, Novo usuário: Adminitrador\_Mestre, Criação de requisitos que possibilitem o **adminitrador\_mestre** gerenciar outros **administradores**. |

