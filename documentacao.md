PARTE 1 — Definição da automação:
Quero criar uma automação no N8N para **atendimento automático de clientes interessados no curso de n8n de uma empresa fictícia**, utilizando inteligência artificial para analisar e responder às dúvidas recebidas por e-mail.

**Público ou responsável:**

Equipe comercial e de atendimento da empresa fictícia, além de clientes e potenciais alunos interessados no curso de n8n.

**Resultado esperado:**

Automatizar o atendimento inicial aos interessados no curso, identificando e-mails externos, interpretando as dúvidas dos clientes com auxílio da inteligência artificial e do Google Gemini e enviando respostas personalizadas diretamente ao e-mail do remetente. O objetivo é reduzir o trabalho manual da equipe, agilizar o atendimento e melhorar a experiência dos potenciais alunos.

PARTE 2 — Planejamento do workflow:
**Ferramentas envolvidas:**

- **n8n:** plataforma responsável por executar e controlar o workflow.
- **E-mail:** serviço utilizado para receber as mensagens e enviar as respostas.
- **Google Gemini:** modelo de inteligência artificial utilizado para interpretar as dúvidas e elaborar respostas.
- **Nó de decisão (IF):** utilizado para verificar se o remetente pertence ao domínio interno da empresa.
- **Integração com IA:** utilizada para processar o conteúdo da mensagem e gerar uma resposta adequada.

**Fluxo desejado:**

1. **Recebimento do e-mail:** o workflow identifica a chegada de uma nova mensagem com dúvidas sobre o curso de n8n.
2. **Verificação do remetente:** o sistema analisa o endereço de e-mail para identificar se a mensagem é interna ou externa.
3. **Tratamento da mensagem:** se o remetente for interno, o fluxo não envia uma resposta automática ao cliente. Se for externo, a mensagem segue para análise.
4. **Análise com inteligência artificial:** o conteúdo do e-mail é encaminhado ao Gemini para identificar as dúvidas e elaborar uma resposta com base nas informações disponíveis sobre o curso.
5. **Envio da resposta:** o n8n envia a resposta gerada pela IA ao endereço de e-mail do cliente.
6. **Finalização:** o workflow encerra a execução após o processamento da mensagem.

**Regras importantes:**

- Não responder automaticamente a e-mails enviados por usuários do domínio interno da empresa.
- Responder somente a mensagens externas que se enquadrem no atendimento sobre o curso de n8n.
- Utilizar informações confiáveis sobre o curso para evitar respostas incorretas.
- Não inventar preços, datas, horários, certificados ou condições de matrícula.
- Preservar o endereço original do remetente para garantir que a resposta seja enviada ao destinatário correto.
- Evitar respostas automáticas a mensagens do próprio sistema, prevenindo ciclos de envio de e-mails.
- Caso a IA não consiga responder com segurança, encaminhar a mensagem para análise humana, em vez de inventar uma informação.

PASSO 3 — Prompt para desenvolver e documentar a automação
Atue como um especialista em automação de processos com n8n, integração de serviços de e-mail e inteligência artificial generativa.

Crie e documente uma automação de atendimento por e-mail para uma empresa fictícia que oferece um curso de n8n.

**Público:**

Clientes e potenciais alunos que enviam e-mails solicitando informações sobre o curso. A equipe interna da empresa também poderá acompanhar as mensagens que precisem de atendimento manual.

**Ferramentas envolvidas:**

- n8n para orquestração do workflow.
- Nó de recebimento ou monitoramento de e-mails.
- Nó IF para verificar se o remetente pertence ao domínio interno da empresa.
- Integração com Google Gemini para interpretar as mensagens e elaborar respostas.
- Nó de envio de e-mail para responder ao cliente.
- Nós adicionais de tratamento de erros e encaminhamento para atendimento humano, quando necessários.

**Fluxo:**

1. Monitorar a caixa de entrada e identificar novos e-mails.
2. Extrair o endereço do remetente, o assunto e o conteúdo da mensagem.
3. Verificar se o remetente pertence ao domínio interno da empresa.
4. Interromper o atendimento automático para mensagens internas.
5. Encaminhar mensagens externas relacionadas ao curso para análise da inteligência artificial.
6. Utilizar o Google Gemini para compreender as dúvidas e produzir uma resposta educada, clara e profissional.
7. Enviar a resposta ao endereço original do cliente por meio do serviço de e-mail configurado.
8. Tratar falhas de processamento, respostas vazias e dúvidas que não possam ser solucionadas com as informações disponíveis.
9. Registrar o resultado da execução para facilitar o acompanhamento e a manutenção do workflow.

**Regras:**

- Não responder a e-mails internos.
- Não inventar informações sobre o curso.
- Utilizar uma base de conhecimento confiável sobre o conteúdo programático, valores, duração, formato e matrícula.
- Não enviar respostas quando não houver informações suficientes para responder com segurança.
- Evitar loops de e-mail, mensagens duplicadas e respostas ao próprio sistema.
- Proteger credenciais, dados pessoais e informações confidenciais.
- Encaminhar casos não resolvidos para análise humana.

**O que deve ser entregue:**

Explique a arquitetura do workflow, os nós do n8n necessários, a configuração de cada nó, as conexões entre eles, as condições de decisão e o tratamento de erros.

Apresente exemplos de e-mails recebidos, da verificação do remetente, das instruções enviadas ao Gemini e das respostas geradas.

Utilize uma empresa fictícia e dados de demonstração. Não invente credenciais nem presuma configurações que ainda não foram fornecidas.

O resultado deve servir como documentação técnica e material de estudo para compreender, testar e aprimorar a automação no n8n.