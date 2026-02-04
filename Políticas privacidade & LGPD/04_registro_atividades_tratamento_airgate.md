# REGISTRO DE ATIVIDADES DE TRATAMENTO DE DADOS PESSOAIS

## AIRGATE TECNOLOGIA LTDA.

**Documento:** RAT-LGPD-001

**Versão:** 1.0

**Data de Atualização:** [DATA]

**Responsável:** [NOME DO DPO]

---

## IDENTIFICAÇÃO DO CONTROLADOR

| Campo | Informação |
|-------|------------|
| **Razão Social** | AIRGATE TECNOLOGIA LTDA. |
| **CNPJ** | [INSERIR] |
| **Endereço** | [INSERIR] |
| **Encarregado (DPO)** | [NOME] |
| **Contato do DPO** | privacidade@airgate.app |

---

## ATIVIDADES DE TRATAMENTO

### AT-001: Cadastro de Anfitriões/Gestores

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-001 |
| **Nome da Atividade** | Cadastro e gestão de conta de anfitriões |
| **Finalidade** | Permitir acesso à plataforma e prestação dos serviços |
| **Base Legal** | Art. 7º, V — Execução de contrato |
| **Categorias de Titulares** | Pessoas físicas e representantes de PJ (anfitriões, gestores de imóveis) |
| **Categorias de Dados** | Nome, e-mail, telefone, CPF/CNPJ, endereço |
| **Classificação** | 🟠 Confidencial |
| **Fonte dos Dados** | Titular (formulário de cadastro) |
| **Compartilhamento** | Processadores de pagamento (dados de cobrança) |
| **Transferência Internacional** | Sim — servidores cloud [REGIÃO] |
| **Prazo de Retenção** | Vigência do contrato + 5 anos |
| **Medidas de Segurança** | Criptografia, controle de acesso, backup |

---

### AT-002: Processamento de Pagamentos

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-002 |
| **Nome da Atividade** | Cobrança de assinaturas e processamento de pagamentos |
| **Finalidade** | Viabilizar a cobrança pelos serviços prestados |
| **Base Legal** | Art. 7º, V — Execução de contrato |
| **Categorias de Titulares** | Anfitriões/gestores pagantes |
| **Categorias de Dados** | Nome, CPF/CNPJ, dados de cartão de crédito, histórico de transações |
| **Classificação** | 🟠 Confidencial |
| **Fonte dos Dados** | Titular (checkout) |
| **Compartilhamento** | Gateway de pagamento [NOME DO GATEWAY] |
| **Transferência Internacional** | Conforme política do gateway |
| **Prazo de Retenção** | 5 anos (legislação tributária) |
| **Medidas de Segurança** | PCI-DSS (via gateway), tokenização |

---

### AT-003: Cadastro de Hóspedes

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-003 |
| **Nome da Atividade** | Registro de hóspedes para controle de acesso |
| **Finalidade** | Criar credenciais de acesso temporárias |
| **Base Legal** | Art. 7º, V — Execução de contrato |
| **Categorias de Titulares** | Hóspedes dos imóveis |
| **Categorias de Dados** | Nome, e-mail ou telefone, período da reserva |
| **Classificação** | 🟠 Confidencial |
| **Fonte dos Dados** | Integração Airbnb/Booking ou cadastro manual pelo anfitrião |
| **Compartilhamento** | Anfitriões (visualizam nome e período) |
| **Transferência Internacional** | Sim — servidores cloud [REGIÃO] |
| **Prazo de Retenção** | 90 dias após término da reserva |
| **Medidas de Segurança** | Criptografia, acesso restrito |

---

### AT-004: Reconhecimento Facial (Biometria)

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-004 |
| **Nome da Atividade** | Autenticação biométrica para controle de acesso |
| **Finalidade** | **EXCLUSIVA:** Autenticar identidade do titular para liberação de acesso |
| **Base Legal** | **Art. 11, I — Consentimento específico e destacado** |
| **Categorias de Titulares** | Hóspedes e anfitriões que optarem pelo recurso |
| **Categorias de Dados** | **DADO SENSÍVEL:** Template biométrico facial |
| **Classificação** | 🔴 **SENSÍVEL** |
| **Fonte dos Dados** | Captura via câmera do dispositivo (com consentimento) |
| **Compartilhamento** | **NENHUM** — dados não são compartilhados |
| **Transferência Internacional** | Sim — servidores cloud [REGIÃO] (criptografado) |
| **Prazo de Retenção** | Até 30 dias após revogação do consentimento ou término do contrato |
| **Medidas de Segurança** | Criptografia AES-256, chave única por usuário, banco isolado, sem acesso humano |
| **RIPD** | **OBRIGATÓRIO** — ver documento RIPD-001 |
| **Termo de Consentimento** | Obrigatório antes da coleta |

---

### AT-005: Registro de Acessos (Logs)

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-005 |
| **Nome da Atividade** | Registro de entradas e saídas nos imóveis |
| **Finalidade** | Histórico de acessos para segurança e auditoria |
| **Base Legal** | Art. 7º, IX — Legítimo interesse |
| **Categorias de Titulares** | Todos os usuários que acessam os imóveis |
| **Categorias de Dados** | ID do usuário, data/hora, método de acesso, status |
| **Classificação** | 🟠 Confidencial |
| **Fonte dos Dados** | Sistema de controle de acesso |
| **Compartilhamento** | Anfitriões (visualizam logs de seus imóveis) |
| **Transferência Internacional** | Sim — servidores cloud [REGIÃO] |
| **Prazo de Retenção** | 6 meses |
| **Medidas de Segurança** | Criptografia, imutabilidade dos logs |

---

### AT-006: Integração com Plataformas de Reserva

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-006 |
| **Nome da Atividade** | Sincronização com Airbnb e Booking.com |
| **Finalidade** | Criar acessos automaticamente a partir de reservas |
| **Base Legal** | Art. 7º, V — Execução de contrato |
| **Categorias de Titulares** | Hóspedes com reservas nas plataformas |
| **Categorias de Dados** | Nome do hóspede, datas de check-in/check-out |
| **Classificação** | 🟠 Confidencial |
| **Fonte dos Dados** | APIs do Airbnb e Booking.com |
| **Compartilhamento** | Não há compartilhamento reverso |
| **Transferência Internacional** | Dados originados de servidores do Airbnb/Booking |
| **Prazo de Retenção** | 90 dias após término da reserva |
| **Medidas de Segurança** | OAuth 2.0, conexões criptografadas |

---

### AT-007: Suporte ao Cliente

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-007 |
| **Nome da Atividade** | Atendimento de solicitações e suporte técnico |
| **Finalidade** | Resolver problemas e responder dúvidas |
| **Base Legal** | Art. 7º, V — Execução de contrato |
| **Categorias de Titulares** | Anfitriões, gestores, hóspedes |
| **Categorias de Dados** | Nome, e-mail, histórico de conversas, dados técnicos do problema |
| **Classificação** | 🟡 Interno |
| **Fonte dos Dados** | Canais de atendimento (e-mail, chat, telefone) |
| **Compartilhamento** | Não há |
| **Transferência Internacional** | Conforme ferramenta de help desk utilizada |
| **Prazo de Retenção** | 2 anos |
| **Medidas de Segurança** | Acesso restrito à equipe de suporte |

---

### AT-008: Analytics e Métricas

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-008 |
| **Nome da Atividade** | Análise de uso da plataforma |
| **Finalidade** | Melhorar produtos e serviços |
| **Base Legal** | Art. 7º, IX — Legítimo interesse |
| **Categorias de Titulares** | Todos os usuários |
| **Categorias de Dados** | Dados agregados e anonimizados (não identificáveis) |
| **Classificação** | 🟢 Público (após anonimização) |
| **Fonte dos Dados** | Eventos da plataforma |
| **Compartilhamento** | Não há (dados anonimizados) |
| **Transferência Internacional** | Conforme ferramenta de analytics |
| **Prazo de Retenção** | Indefinido (dados anonimizados) |
| **Medidas de Segurança** | Anonimização antes do processamento |

---

### AT-009: Atendimento a Solicitações de Titulares

| Campo | Descrição |
|-------|-----------|
| **ID** | AT-009 |
| **Nome da Atividade** | Gestão de direitos dos titulares (LGPD) |
| **Finalidade** | Atender solicitações de acesso, correção, eliminação, etc. |
| **Base Legal** | Art. 18 — Direitos do titular |
| **Categorias de Titulares** | Qualquer titular que faça solicitação |
| **Categorias de Dados** | Dados necessários para identificação e atendimento |
| **Classificação** | 🟠 Confidencial |
| **Fonte dos Dados** | Solicitação do titular |
| **Compartilhamento** | Não há |
| **Transferência Internacional** | Não |
| **Prazo de Retenção** | 5 anos (comprovação de atendimento) |
| **Medidas de Segurança** | Acesso restrito ao DPO |

---

## RESUMO POR BASE LEGAL

| Base Legal | Atividades |
|------------|------------|
| **Consentimento (Art. 7º, I)** | Cookies não essenciais |
| **Consentimento específico (Art. 11, I)** | AT-004 (Biometria) |
| **Obrigação legal (Art. 7º, II)** | Emissão de notas fiscais, guarda de logs |
| **Execução de contrato (Art. 7º, V)** | AT-001, AT-002, AT-003, AT-006, AT-007 |
| **Legítimo interesse (Art. 7º, IX)** | AT-005, AT-008 |

---

## RESUMO POR CLASSIFICAÇÃO

| Classificação | Atividades |
|---------------|------------|
| 🔴 **SENSÍVEL** | AT-004 (Biometria) |
| 🟠 **CONFIDENCIAL** | AT-001, AT-002, AT-003, AT-005, AT-006, AT-009 |
| 🟡 **INTERNO** | AT-007 |
| 🟢 **PÚBLICO** | AT-008 (após anonimização) |

---

## OPERADORES (FORNECEDORES)

| Operador | Serviço | Atividades Relacionadas | Contrato LGPD | País |
|----------|---------|------------------------|---------------|------|
| [AWS/GCP/Azure] | Infraestrutura cloud | Todas | ✅ Sim | [PAÍS] |
| [Gateway pagamento] | Processamento de pagamentos | AT-002 | ✅ Sim | [PAÍS] |
| [Ferramenta de e-mail] | Envio de e-mails | AT-001, AT-003 | ✅ Sim | [PAÍS] |
| [Help desk] | Suporte ao cliente | AT-007 | ✅ Sim | [PAÍS] |
| [Analytics] | Métricas | AT-008 | ✅ Sim | [PAÍS] |

---

## TRANSFERÊNCIAS INTERNACIONAIS

| Destino | Mecanismo de Adequação | Atividades |
|---------|------------------------|------------|
| [EUA] | Cláusulas contratuais padrão | AT-001 a AT-008 |
| [UE] | Decisão de adequação | [se aplicável] |

---

## HISTÓRICO DE ATUALIZAÇÕES

| Data | Versão | Responsável | Alteração |
|------|--------|-------------|-----------|
| [DATA] | 1.0 | [DPO] | Criação do documento |

---

## PRÓXIMA REVISÃO

**Data prevista:** [DATA + 6 meses]

**Responsável:** [DPO]

---

*Este documento deve ser mantido atualizado e disponibilizado à ANPD quando solicitado, conforme Art. 37 da LGPD.*

---

**AIRGATE TECNOLOGIA LTDA.**

Encarregado de Proteção de Dados: [NOME]

E-mail: privacidade@airgate.app
