# DIRETIVAS INTERNAS DE PROTEÇÃO DE DADOS PESSOAIS

## AIRGATE TECNOLOGIA LTDA.

**Documento:** DIR-LGPD-001

**Versão:** 1.0

**Classificação:** INTERNO — USO RESTRITO

**Vigência:** A partir de [DATA]

**Aprovação:** [NOME DO RESPONSÁVEL], [CARGO]

---

## SUMÁRIO

1. Objetivo e Escopo
2. Definições
3. Princípios Gerais
4. Governança de Dados
5. Classificação de Dados
6. Regras para Dados Biométricos
7. Ciclo de Vida dos Dados
8. Direitos dos Titulares
9. Segurança da Informação
10. Resposta a Incidentes
11. Treinamento e Conscientização
12. Fornecedores e Terceiros
13. Auditoria e Conformidade
14. Sanções
15. Anexos

---

## 1. OBJETIVO E ESCOPO

### 1.1 Objetivo

Este documento estabelece as diretivas internas obrigatórias para todos os colaboradores, prestadores de serviço e parceiros da Airgate no que se refere ao tratamento de dados pessoais, em conformidade com a Lei Geral de Proteção de Dados Pessoais (Lei nº 13.709/2018 — LGPD).

### 1.2 Escopo

Aplica-se a:

- Todos os colaboradores (CLT, PJ, estagiários, temporários)
- Prestadores de serviço com acesso a dados pessoais
- Fornecedores e parceiros comerciais
- Todos os sistemas, processos e atividades que envolvam dados pessoais

### 1.3 Documentos Relacionados

| Documento | Descrição |
|-----------|-----------|
| Política de Privacidade | Documento público para titulares |
| Termo de Consentimento Biométrico | Coleta de consentimento para dados sensíveis |
| Política de Segurança da Informação | Controles técnicos de segurança |
| Plano de Resposta a Incidentes | Procedimentos em caso de violação |

---

## 2. DEFINIÇÕES

### 2.1 Glossário

| Termo | Definição |
|-------|-----------|
| **Dado Pessoal** | Informação relacionada a pessoa natural identificada ou identificável |
| **Dado Sensível** | Dado sobre origem racial/étnica, convicção religiosa, opinião política, saúde, vida sexual, **dado biométrico** |
| **Titular** | Pessoa natural a quem se referem os dados |
| **Controlador** | Airgate — decide sobre o tratamento |
| **Operador** | Quem trata dados em nome do controlador |
| **DPO/Encarregado** | Responsável pela proteção de dados na Airgate |
| **ANPD** | Autoridade Nacional de Proteção de Dados |
| **RIPD** | Relatório de Impacto à Proteção de Dados |
| **Incidente** | Evento que comprometa confidencialidade, integridade ou disponibilidade de dados |

### 2.2 Níveis de Classificação de Dados

| Nível | Descrição | Exemplos |
|-------|-----------|----------|
| 🔴 **SENSÍVEL** | Dados que exigem proteção máxima | Dados biométricos |
| 🟠 **CONFIDENCIAL** | Dados pessoais que exigem restrição de acesso | CPF, endereço, dados financeiros |
| 🟡 **INTERNO** | Dados de uso interno da empresa | E-mails corporativos, documentos internos |
| 🟢 **PÚBLICO** | Dados de conhecimento público | Informações do site, materiais de marketing |

---

## 3. PRINCÍPIOS GERAIS

### 3.1 Princípios da LGPD (Art. 6º)

Todo tratamento de dados na Airgate deve observar:

| Princípio | Descrição | Aplicação Prática |
|-----------|-----------|-------------------|
| **Finalidade** | Propósitos legítimos, específicos e informados | Não usar dados para fins diferentes do informado |
| **Adequação** | Compatível com as finalidades | Coletar apenas dados necessários para o serviço |
| **Necessidade** | Mínimo necessário | Não solicitar dados além do estritamente necessário |
| **Livre acesso** | Consulta facilitada ao titular | Responder solicitações em até 15 dias |
| **Qualidade** | Dados exatos e atualizados | Manter cadastros atualizados |
| **Transparência** | Informações claras ao titular | Linguagem simples na comunicação |
| **Segurança** | Proteção contra acessos não autorizados | Criptografia, controle de acesso |
| **Prevenção** | Prevenir danos aos titulares | Avaliação de riscos antes de novos tratamentos |
| **Não discriminação** | Não usar dados para discriminar | Vedado uso de dados sensíveis para exclusão |
| **Responsabilização** | Demonstrar conformidade | Documentar todas as atividades de tratamento |

### 3.2 Regra de Ouro

> **"NA DÚVIDA, NÃO COLETE. NA DÚVIDA, NÃO COMPARTILHE. NA DÚVIDA, CONSULTE O DPO."**

---

## 4. GOVERNANÇA DE DADOS

### 4.1 Estrutura de Responsabilidades

```
┌─────────────────────────────────────────────────────┐
│                    DIRETORIA                        │
│         (Responsabilidade final - Controlador)       │
└─────────────────────┬───────────────────────────────┘
                      │
┌─────────────────────▼───────────────────────────────┐
│            ENCARREGADO (DPO)                        │
│    • Ponto focal LGPD                               │
│    • Canal com titulares e ANPD                     │
│    • Orientação e treinamento                       │
└─────────────────────┬───────────────────────────────┘
                      │
┌─────────────────────▼───────────────────────────────┐
│              COMITÊ DE PRIVACIDADE                  │
│    • DPO + Jurídico + TI + Produto                 │
│    • Reuniões mensais                               │
│    • Decisões sobre tratamentos críticos            │
└─────────────────────┬───────────────────────────────┘
                      │
┌─────────────────────▼───────────────────────────────┐
│           TODOS OS COLABORADORES                    │
│    • Cumprir estas diretivas                        │
│    • Reportar incidentes                            │
│    • Participar de treinamentos                     │
└─────────────────────────────────────────────────────┘
```

### 4.2 Encarregado de Proteção de Dados (DPO)

**Identificação:**
- Nome: [INSERIR NOME]
- E-mail: privacidade@airgate.app
- Telefone: [INSERIR]

**Atribuições:**
1. Receber e responder solicitações de titulares
2. Receber comunicações da ANPD
3. Orientar colaboradores sobre proteção de dados
4. Aprovar novos tratamentos de dados sensíveis
5. Conduzir avaliações de impacto (RIPD)
6. Gerenciar incidentes de segurança
7. Manter registros de tratamento atualizados

### 4.3 Comitê de Privacidade

**Composição:**
- DPO (coordenador)
- Representante jurídico
- Representante de TI/Segurança
- Representante de Produto

**Reuniões:** Mensais (ou extraordinárias em caso de incidentes)

**Decisões:**
- Aprovação de novos tratamentos de dados sensíveis
- Avaliação de fornecedores críticos
- Resposta a incidentes de alto impacto
- Atualização de políticas e procedimentos

---

## 5. CLASSIFICAÇÃO DE DADOS

### 5.1 Inventário de Dados da Airgate

| Categoria | Dados | Classificação | Base Legal |
|-----------|-------|---------------|------------|
| **Cadastro Anfitrião** | Nome, e-mail, telefone, CPF/CNPJ | 🟠 Confidencial | Execução de contrato |
| **Pagamento** | Dados de cartão, conta bancária | 🟠 Confidencial | Execução de contrato |
| **Hóspede** | Nome, contato, período reserva | 🟠 Confidencial | Execução de contrato |
| **Biométrico** | Template facial | 🔴 **SENSÍVEL** | **Consentimento específico** |
| **Acesso** | Logs de entrada/saída | 🟠 Confidencial | Legítimo interesse |
| **Navegação** | IP, cookies, dispositivo | 🟡 Interno | Legítimo interesse |

### 5.2 Mapeamento de Fluxo de Dados

Todo novo processo ou sistema que envolva dados pessoais deve:

1. Ser documentado no Registro de Atividades de Tratamento
2. Ter base legal identificada
3. Ser aprovado pelo DPO (obrigatório para dados sensíveis)
4. Ter medidas de segurança definidas

---

## 6. REGRAS PARA DADOS BIOMÉTRICOS

### ⚠️ SEÇÃO CRÍTICA — LEITURA OBRIGATÓRIA

Os dados biométricos (reconhecimento facial) são **DADOS PESSOAIS SENSÍVEIS** e exigem tratamento especial.

### 6.1 Regras Obrigatórias

| Regra | Descrição | Consequência do Descumprimento |
|-------|-----------|-------------------------------|
| **R1** | Consentimento obrigatório | NUNCA coletar biometria sem termo assinado |
| **R2** | Finalidade única | APENAS para autenticação de acesso |
| **R3** | Sem compartilhamento | NUNCA enviar para terceiros |
| **R4** | Sem acesso humano | Nenhum colaborador visualiza os templates |
| **R5** | Criptografia obrigatória | Sempre criptografado (trânsito e repouso) |
| **R6** | Eliminação em 30 dias | Após revogação ou término do contrato |
| **R7** | Registro de operações | Todo acesso ao banco biométrico é logado |

### 6.2 Fluxo de Coleta de Dados Biométricos

```
┌─────────────────────────────────────────────────────┐
│ 1. APRESENTAÇÃO DO TERMO DE CONSENTIMENTO           │
│    • Específico e destacado                         │
│    • Explicar finalidade e direitos                 │
│    • Informar alternativas (QR Code, senha)         │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 2. COLETA DO CONSENTIMENTO                          │
│    • Assinatura física OU aceite eletrônico         │
│    • Registrar data, hora, IP, versão do termo      │
│    • Armazenar comprovante                          │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 3. CAPTURA DA BIOMETRIA                             │
│    • Imagem temporária apenas                       │
│    • Extração do template                           │
│    • Descarte imediato da imagem                    │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 4. ARMAZENAMENTO                                    │
│    • Template criptografado (AES-256)               │
│    • Banco de dados isolado                         │
│    • Chave única por usuário                        │
└─────────────────────────────────────────────────────┘
```

### 6.3 Checklist de Conformidade Biométrica

Antes de qualquer operação com dados biométricos, verificar:

- [ ] Termo de Consentimento assinado e arquivado?
- [ ] Consentimento vigente (não revogado)?
- [ ] Operação está dentro da finalidade autorizada?
- [ ] Dados serão criptografados?
- [ ] Nenhum compartilhamento não autorizado?
- [ ] Log da operação será registrado?

### 6.4 Proibições Absolutas

❌ **NUNCA** armazenar a imagem facial original (apenas template)

❌ **NUNCA** acessar dados biométricos sem necessidade técnica comprovada

❌ **NUNCA** compartilhar dados biométricos com anfitriões ou terceiros

❌ **NUNCA** usar dados biométricos para marketing ou perfilamento

❌ **NUNCA** coletar biometria de menores sem consentimento do responsável

❌ **NUNCA** condicionar o serviço à entrega de dados biométricos (é opcional)

---

## 7. CICLO DE VIDA DOS DADOS

### 7.1 Coleta

**Regras:**
- Coletar apenas dados necessários (princípio da minimização)
- Informar o titular sobre a coleta
- Verificar existência de base legal
- Para dados sensíveis: consentimento específico obrigatório

**Checklist de Coleta:**
- [ ] Base legal identificada?
- [ ] Titular informado?
- [ ] Dados são realmente necessários?
- [ ] Formulário/sistema aprovado pelo DPO?

### 7.2 Armazenamento

**Regras:**
- Dados confidenciais e sensíveis: sempre criptografados
- Controle de acesso por perfil (need-to-know)
- Backups criptografados
- Segregação de ambientes (produção/desenvolvimento)

**Proibições:**
- ❌ Armazenar dados em computadores pessoais
- ❌ Armazenar dados em serviços não aprovados (Dropbox pessoal, Google Drive pessoal)
- ❌ Enviar dados por e-mail sem criptografia
- ❌ Manter cópias desnecessárias

### 7.3 Uso e Processamento

**Regras:**
- Usar dados apenas para finalidade informada
- Registrar operações de tratamento
- Anonimizar dados quando possível (analytics)
- Pseudonimizar dados de desenvolvimento/testes

### 7.4 Compartilhamento

**Regras:**
- Apenas com fornecedores aprovados (contrato com cláusulas LGPD)
- Registro de todos os compartilhamentos
- Verificar se titular foi informado
- Para dados sensíveis: verificar se há autorização específica

**Aprovações Necessárias:**

| Tipo de Compartilhamento | Aprovador |
|--------------------------|-----------|
| Com fornecedor existente | Gestor da área |
| Com novo fornecedor | DPO + Comitê de Privacidade |
| Dados sensíveis | DPO (obrigatório) |
| Transferência internacional | DPO + Jurídico |

### 7.5 Eliminação

**Prazos de Retenção:**

| Tipo de Dado | Prazo | Após o Prazo |
|--------------|-------|--------------|
| Dados cadastrais | Vigência + 5 anos | Eliminação |
| Dados de pagamento | 5 anos (fiscal) | Eliminação |
| Logs de acesso | 6 meses | Eliminação |
| **Dados biométricos** | **Até 30 dias após revogação/término** | **Eliminação irreversível** |
| Dados de hóspedes | 90 dias após reserva | Eliminação |

**Processo de Eliminação:**
1. Verificar se não há obrigação legal de guarda
2. Eliminar de todos os sistemas (produção, backup, logs)
3. Registrar a eliminação (data, responsável, método)
4. Para dados biométricos: emitir certificado de eliminação

---

## 8. DIREITOS DOS TITULARES

### 8.1 Direitos Garantidos

| Direito | Prazo de Atendimento | Responsável |
|---------|---------------------|-------------|
| Confirmação de tratamento | 15 dias | DPO |
| Acesso aos dados | 15 dias | DPO |
| Correção | 15 dias | DPO + Área responsável |
| Eliminação | 15 dias | DPO + TI |
| Portabilidade | 15 dias | DPO + TI |
| Revogação de consentimento | Imediato | Sistema/DPO |
| Informação sobre compartilhamento | 15 dias | DPO |
| Oposição | 15 dias | DPO |

### 8.2 Procedimento de Atendimento

```
┌─────────────────────────────────────────────────────┐
│ 1. RECEBIMENTO DA SOLICITAÇÃO                       │
│    • Canal: privacidade@airgate.app                 │
│    • Registrar: data, titular, tipo de solicitação  │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 2. VERIFICAÇÃO DE IDENTIDADE                        │
│    • Confirmar que solicitante é o titular          │
│    • Solicitar documento se necessário              │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 3. ANÁLISE DA SOLICITAÇÃO                           │
│    • Verificar viabilidade técnica e legal          │
│    • Consultar áreas envolvidas                     │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 4. EXECUÇÃO                                         │
│    • Realizar a ação solicitada                     │
│    • Documentar                                     │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 5. RESPOSTA AO TITULAR                              │
│    • Prazo máximo: 15 dias                          │
│    • Informar ação realizada ou justificar negativa │
└─────────────────────────────────────────────────────┘
```

### 8.3 Modelo de Resposta

Ver Anexo A — Modelos de Comunicação com Titulares

---

## 9. SEGURANÇA DA INFORMAÇÃO

### 9.1 Controles Obrigatórios

| Controle | Aplicação | Responsável |
|----------|-----------|-------------|
| Criptografia em trânsito | TLS 1.3 em todas as conexões | TI |
| Criptografia em repouso | AES-256 para dados sensíveis | TI |
| Autenticação forte | MFA para todos os colaboradores | TI |
| Controle de acesso | Perfis por função (RBAC) | TI + Gestores |
| Logs de auditoria | Registro de acessos e operações | TI |
| Backup seguro | Criptografado, testado mensalmente | TI |
| Firewall/WAF | Proteção de perímetro | TI |
| Antivírus/EDR | Em todos os endpoints | TI |

### 9.2 Regras de Acesso

**Princípio do Menor Privilégio:** Cada colaborador deve ter acesso apenas aos dados necessários para sua função.

| Perfil | Acesso Permitido |
|--------|------------------|
| Suporte Nível 1 | Dados cadastrais básicos (nome, e-mail) |
| Suporte Nível 2 | Dados cadastrais completos, logs de acesso |
| Desenvolvimento | Dados anonimizados/pseudonimizados apenas |
| Financeiro | Dados de pagamento, notas fiscais |
| DPO | Todos os dados (para atender solicitações) |
| **Ninguém** | Visualização direta de dados biométricos |

### 9.3 Regras para Desenvolvimento

- ❌ **NUNCA** usar dados reais em ambiente de desenvolvimento
- ✅ Usar dados fictícios ou anonimizados
- ✅ Sanitizar logs antes de analisar (remover dados pessoais)
- ✅ Implementar privacy by design em novos recursos

---

## 10. RESPOSTA A INCIDENTES

### 10.1 O Que É um Incidente de Dados Pessoais

Qualquer evento que comprometa:
- **Confidencialidade:** Acesso não autorizado a dados
- **Integridade:** Alteração indevida de dados
- **Disponibilidade:** Perda ou destruição de dados

**Exemplos:**
- Vazamento de base de dados
- Ransomware que criptografa dados de clientes
- Envio acidental de dados para destinatário errado
- Perda de dispositivo com dados pessoais
- Acesso indevido por ex-colaborador

### 10.2 Fluxo de Resposta

```
┌─────────────────────────────────────────────────────┐
│ 1. DETECÇÃO E COMUNICAÇÃO IMEDIATA                  │
│    • Qualquer colaborador que detectar             │
│    • Comunicar IMEDIATAMENTE ao DPO                │
│    • E-mail: incidente@airgate.app                 │
│    • Telefone: [NÚMERO DE EMERGÊNCIA]              │
└─────────────────────┬───────────────────────────────┘
                      ▼ (máximo 1 hora)
┌─────────────────────────────────────────────────────┐
│ 2. CONTENÇÃO                                        │
│    • Isolar sistemas afetados                       │
│    • Bloquear acessos comprometidos                 │
│    • Preservar evidências                           │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 3. AVALIAÇÃO                                        │
│    • Determinar escopo (dados e titulares afetados)│
│    • Avaliar risco aos titulares                   │
│    • Decidir sobre comunicação à ANPD e titulares  │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 4. COMUNICAÇÃO (se necessário)                      │
│    • ANPD: prazo razoável (recomendado 72h)        │
│    • Titulares: se houver risco de dano            │
└─────────────────────┬───────────────────────────────┘
                      ▼
┌─────────────────────────────────────────────────────┐
│ 5. REMEDIAÇÃO E LIÇÕES APRENDIDAS                   │
│    • Corrigir vulnerabilidades                      │
│    • Documentar incidente                           │
│    • Atualizar controles preventivos                │
└─────────────────────────────────────────────────────┘
```

### 10.3 Critérios para Comunicação à ANPD

Comunicar à ANPD quando o incidente puder acarretar **risco ou dano relevante** aos titulares:

| Fator | Alto Risco | Baixo Risco |
|-------|-----------|-------------|
| Tipo de dado | Sensível, financeiro | Cadastral básico |
| Volume | Grande número de titulares | Poucos titulares |
| Reversibilidade | Dados expostos publicamente | Dados recuperados rapidamente |
| Dano potencial | Fraude, discriminação | Inconveniência menor |

### 10.4 Contatos de Emergência

| Função | Nome | Telefone | E-mail |
|--------|------|----------|--------|
| DPO | [NOME] | [TEL] | privacidade@airgate.app |
| TI/Segurança | [NOME] | [TEL] | seguranca@airgate.app |
| Jurídico | [NOME] | [TEL] | juridico@airgate.app |
| Direção | [NOME] | [TEL] | [EMAIL] |

---

## 11. TREINAMENTO E CONSCIENTIZAÇÃO

### 11.1 Programa de Treinamento

| Treinamento | Público | Frequência | Duração |
|-------------|---------|------------|---------|
| **Onboarding LGPD** | Novos colaboradores | Na admissão | 2 horas |
| **Reciclagem anual** | Todos | Anual | 1 hora |
| **Dados sensíveis** | TI, Produto, Suporte | Semestral | 2 horas |
| **Resposta a incidentes** | TI, DPO | Trimestral | 1 hora |

### 11.2 Conteúdo Obrigatório

1. Conceitos básicos da LGPD
2. Tipos de dados pessoais (comum vs sensível)
3. Princípios do tratamento
4. Direitos dos titulares
5. Regras específicas para dados biométricos
6. Como identificar e reportar incidentes
7. Consequências do descumprimento

### 11.3 Registro

Todos os treinamentos devem ser registrados com:
- Lista de presença assinada
- Data e conteúdo ministrado
- Avaliação de conhecimento (quando aplicável)

---

## 12. FORNECEDORES E TERCEIROS

### 12.1 Due Diligence de Fornecedores

Antes de contratar fornecedor com acesso a dados pessoais:

- [ ] Verificar política de privacidade do fornecedor
- [ ] Avaliar medidas de segurança
- [ ] Verificar certificações (ISO 27001, SOC 2, etc.)
- [ ] Confirmar localização dos servidores
- [ ] Aprovar com DPO

### 12.2 Cláusulas Contratuais Obrigatórias

Todo contrato com fornecedor que trate dados pessoais deve incluir:

1. **Definição de papéis:** Controlador vs Operador
2. **Finalidade:** Descrição clara do tratamento autorizado
3. **Segurança:** Obrigação de medidas técnicas e organizacionais
4. **Subcontratação:** Necessidade de aprovação prévia
5. **Confidencialidade:** Obrigação de sigilo
6. **Auditoria:** Direito de verificar conformidade
7. **Incidentes:** Obrigação de notificação imediata
8. **Término:** Obrigação de devolução/eliminação dos dados
9. **Indenização:** Responsabilidade por descumprimento

### 12.3 Fornecedores Aprovados

| Fornecedor | Serviço | Dados Tratados | Localização | Contrato LGPD |
|------------|---------|----------------|-------------|---------------|
| [AWS/GCP/Azure] | Infraestrutura | Todos | [LOCAL] | ✅ |
| [Stripe/Pagar.me] | Pagamentos | Financeiros | [LOCAL] | ✅ |
| [SendGrid/Mailgun] | E-mail | Cadastrais | [LOCAL] | ✅ |

---

## 13. AUDITORIA E CONFORMIDADE

### 13.1 Registro de Atividades de Tratamento

O DPO mantém registro atualizado de:

- Todas as atividades de tratamento
- Bases legais aplicáveis
- Categorias de dados e titulares
- Compartilhamentos realizados
- Prazos de retenção
- Medidas de segurança

### 13.2 Relatório de Impacto (RIPD)

Elaborar RIPD para tratamentos que apresentem **alto risco**, incluindo:

- Todo tratamento de dados biométricos
- Decisões automatizadas
- Tratamento em larga escala
- Novos produtos/funcionalidades com dados sensíveis

### 13.3 Auditorias

| Tipo | Frequência | Responsável |
|------|------------|-------------|
| Autoavaliação | Trimestral | DPO |
| Auditoria interna | Anual | Comitê de Privacidade |
| Auditoria externa | Bienal (recomendado) | Consultoria especializada |

---

## 14. SANÇÕES

### 14.1 Consequências do Descumprimento

O descumprimento destas diretivas pode resultar em:

| Gravidade | Exemplos | Consequência |
|-----------|----------|--------------|
| **Leve** | Não participar de treinamento | Advertência verbal |
| **Média** | Compartilhar dados sem autorização | Advertência formal |
| **Grave** | Acessar dados biométricos indevidamente | Suspensão + processo administrativo |
| **Gravíssima** | Vazar dados intencionalmente | Demissão por justa causa + medidas legais |

### 14.2 Sanções da LGPD

A Airgate está sujeita às sanções previstas na LGPD (Art. 52):

- Advertência
- Multa de até 2% do faturamento (limitada a R$ 50 milhões por infração)
- Publicização da infração
- Bloqueio ou eliminação dos dados
- Suspensão do funcionamento do banco de dados
- Proibição parcial ou total do exercício de atividades relacionadas a tratamento de dados

---

## 15. ANEXOS

### Anexo A — Modelos de Comunicação com Titulares

[Incluir modelos de e-mail para: confirmação de recebimento de solicitação, resposta a pedido de acesso, resposta a pedido de eliminação, etc.]

### Anexo B — Formulário de Registro de Incidente

[Incluir formulário padrão para registro de incidentes]

### Anexo C — Checklist de Avaliação de Fornecedor

[Incluir checklist de due diligence]

### Anexo D — Modelo de Cláusulas Contratuais LGPD

[Incluir modelo de cláusulas para contratos com fornecedores]

---

## CONTROLE DE VERSÕES

| Versão | Data | Autor | Alterações |
|--------|------|-------|------------|
| 1.0 | [DATA] | [DPO] | Versão inicial |

---

## TERMO DE CIÊNCIA

Declaro que li, compreendi e me comprometo a cumprir integralmente as Diretivas Internas de Proteção de Dados Pessoais da Airgate.

**Nome:** _____________________________________________

**Cargo:** ____________________________________________

**Data:** ____/____/________

**Assinatura:** ________________________________________

---

**AIRGATE TECNOLOGIA LTDA.**

*Documento de uso interno — Proibida reprodução ou distribuição externa sem autorização.*
