# FLUXO DE ACEITE — GUIA DE IMPLEMENTAÇÃO

## AIRGATE

**Documento:** FLUXO-ACEITE-001

**Versão:** 1.0

---

## 1. Visão Geral

Este documento descreve como implementar o aceite dos Termos de Uso e Política de Privacidade no produto AirGate, de forma juridicamente válida e com boa experiência de usuário.

---

## 2. Tipos de Aceite

| Tipo | Quando Usar | Validade Jurídica |
|------|-------------|-------------------|
| **Click-wrap** | Cadastro online, upgrade de plano | ✅ Alta (com registro adequado) |
| **Browse-wrap** | Navegação no site | ⚠️ Baixa (evitar para obrigações importantes) |
| **Assinatura digital** | Contratos enterprise, alto valor | ✅ Muito alta |
| **Assinatura física** | Exceções, clientes que exigem | ✅ Muito alta |

**Recomendação:** Usar **click-wrap** para 90% dos casos, reservando assinatura digital para clientes enterprise.

---

## 3. Fluxo de Cadastro (Click-wrap)

### 3.1 Tela de Cadastro

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│                    🔐 Criar sua conta                       │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Nome completo                                        │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ E-mail                                               │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Telefone (WhatsApp)                                  │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ Senha                                                │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ CPF ou CNPJ                                          │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ─────────────────────────────────────────────────────────  │
│                                                             │
│  ☑️ Li e concordo com os [Termos de Uso] e                 │
│     [Política de Privacidade]                              │
│                                                             │
│           ┌─────────────────────────┐                      │
│           │    CRIAR CONTA          │                      │
│           └─────────────────────────┘                      │
│                                                             │
│  Já tem conta? [Fazer login]                               │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 3.2 Requisitos Técnicos

| Requisito | Implementação |
|-----------|---------------|
| **Checkbox obrigatório** | Botão "Criar Conta" só habilita após marcar |
| **Links funcionais** | "Termos de Uso" e "Política de Privacidade" abrem em nova aba |
| **Checkbox desmarcado por padrão** | Usuário deve marcar ativamente |
| **Texto legível** | Mínimo 12px, contraste adequado |

### 3.3 O Que Registrar (Log de Aceite)

```json
{
  "user_id": "uuid-do-usuario",
  "email": "cliente@email.com",
  "documento": "cpf-ou-cnpj",
  "aceite": {
    "termos_de_uso": {
      "versao": "1.0",
      "data_aceite": "2026-02-03T14:32:00Z",
      "ip": "189.40.xxx.xxx",
      "user_agent": "Mozilla/5.0...",
      "url_documento": "https://airgate.app/termos-de-uso"
    },
    "politica_privacidade": {
      "versao": "1.0",
      "data_aceite": "2026-02-03T14:32:00Z",
      "ip": "189.40.xxx.xxx",
      "user_agent": "Mozilla/5.0...",
      "url_documento": "https://airgate.app/privacidade"
    }
  }
}
```

**Importante:** Armazenar esse log por **mínimo 5 anos** (prazo prescricional).

---

## 4. Fluxo de Contratação de Plano

### 4.1 Após Cadastro — Escolha de Plano

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              📦 Escolha seu plano AirGate                   │
│                                                             │
│  ┌─────────────────┐ ┌─────────────────┐ ┌────────────────┐│
│  │  GARAGE         │ │  BASIC          │ │  AIRGATE+      ││
│  │                 │ │                 │ │                ││
│  │  Abertura de    │ │  Tudo do Garage │ │  Tudo do Basic ││
│  │  garagem        │ │  + Acessos auto │ │  + Logs        ││
│  │                 │ │  + Painel       │ │  + Suporte 24h ││
│  │                 │ │                 │ │                ││
│  │  R$ 39/mês      │ │  R$ 99/mês      │ │  R$ 119/mês    ││
│  │  (1 unidade)    │ │  (1 unidade)    │ │  (1 unidade)   ││
│  │                 │ │                 │ │                ││
│  │  [SELECIONAR]   │ │  [SELECIONAR]   │ │  [SELECIONAR]  ││
│  └─────────────────┘ └─────────────────┘ └────────────────┘│
│                                                             │
│  💡 Tem 4+ unidades? Preços especiais a partir de          │
│     R$ 19/unid. [Ver tabela completa]                      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 4.2 Tela de Confirmação de Contratação

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              ✅ Confirmar contratação                       │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  RESUMO DO PEDIDO                                    │   │
│  │                                                      │   │
│  │  Plano: AirGate Basic                               │   │
│  │  Unidades: 2                                        │   │
│  │  Valor mensal: R$ 158,00 (2x R$ 79,00)             │   │
│  │                                                      │   │
│  │  Equipamentos:                                       │   │
│  │  - 1x AirGate Smart Box: R$ 2.695,00               │   │
│  │  - 1x Gateway Garagem: R$ 840,00                    │   │
│  │                                                      │   │
│  │  ─────────────────────────────────────────────────  │   │
│  │  TOTAL HOJE: R$ 3.693,00                           │   │
│  │  (equipamentos + 1ª mensalidade)                    │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ─────────────────────────────────────────────────────────  │
│                                                             │
│  ☑️ Li e concordo com o [Contrato de Prestação de          │
│     Serviços], incluindo as condições de pagamento,        │
│     cancelamento e limitações de responsabilidade.         │
│                                                             │
│  ☐ Quero receber novidades e dicas por e-mail (opcional)   │
│                                                             │
│           ┌─────────────────────────┐                      │
│           │  CONFIRMAR E PAGAR      │                      │
│           └─────────────────────────┘                      │
│                                                             │
│  🔒 Pagamento seguro via Boleto ou PIX                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 4.3 Pontos Importantes

| Elemento | Requisito |
|----------|-----------|
| **Resumo claro dos valores** | Usuário deve ver exatamente o que está pagando |
| **Link para contrato completo** | Deve abrir o PDF/página do contrato |
| **Checkbox separado para marketing** | LGPD exige consentimento separado |
| **Botão com texto claro** | "Confirmar e Pagar" (não apenas "Continuar") |

---

## 5. Fluxo de Aceite de Hóspede (Biometria)

### 5.1 Quando o Hóspede Cadastra Facial

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              📸 Cadastro de Reconhecimento Facial           │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                                                      │   │
│  │    O anfitrião disponibilizou acesso por            │   │
│  │    reconhecimento facial para maior comodidade.     │   │
│  │                                                      │   │
│  │    Isso é OPCIONAL. Você também pode usar           │   │
│  │    o QR Code ou código numérico.                    │   │
│  │                                                      │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ─────────────────────────────────────────────────────────  │
│                                                             │
│  📋 TERMO DE CONSENTIMENTO PARA DADOS BIOMÉTRICOS          │
│                                                             │
│  Ao prosseguir, você autoriza a coleta da sua imagem       │
│  facial EXCLUSIVAMENTE para autenticação de acesso         │
│  ao imóvel durante o período da sua reserva.               │
│                                                             │
│  • A imagem original NÃO é armazenada                      │
│  • Seus dados são criptografados                           │
│  • Serão excluídos em até 30 dias após o checkout          │
│  • Você pode revogar a qualquer momento                    │
│                                                             │
│  [Ler termo completo]                                       │
│                                                             │
│  ─────────────────────────────────────────────────────────  │
│                                                             │
│  ☑️ Li e AUTORIZO o uso dos meus dados biométricos         │
│     conforme descrito acima.                               │
│                                                             │
│   ┌──────────────────┐    ┌──────────────────┐            │
│   │ USAR QR CODE     │    │ CADASTRAR FACIAL │            │
│   │ (sem biometria)  │    │                  │            │
│   └──────────────────┘    └──────────────────┘            │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 5.2 Requisitos LGPD para Biometria

| Requisito | Como Implementar |
|-----------|------------------|
| **Consentimento específico** | Checkbox exclusivo para biometria |
| **Consentimento destacado** | Tela separada, não misturada com outros aceites |
| **Informar finalidade** | "Exclusivamente para autenticação de acesso" |
| **Informar alternativa** | Mostrar opção de QR Code claramente |
| **Permitir recusa sem prejuízo** | Botão "Usar QR Code" com mesmo destaque |
| **Registrar consentimento** | Log com data, hora, IP, versão do termo |

### 5.3 Log de Consentimento Biométrico

```json
{
  "hospede_id": "uuid-do-hospede",
  "reserva_id": "uuid-da-reserva",
  "consentimento_biometrico": {
    "concedido": true,
    "versao_termo": "1.0",
    "data_consentimento": "2026-02-03T18:45:00Z",
    "ip": "200.xxx.xxx.xxx",
    "user_agent": "Mozilla/5.0...",
    "metodo_alternativo_informado": true,
    "data_prevista_exclusao": "2026-02-10"
  }
}
```

---

## 6. Atualização de Termos

### 6.1 Quando Atualizar os Termos

Ao alterar os Termos de Uso ou Política de Privacidade:

1. **Incrementar versão** (ex: 1.0 → 1.1 ou 2.0 para mudanças significativas)
2. **Notificar usuários ativos** por e-mail com 30 dias de antecedência
3. **Exibir banner** no painel solicitando aceite da nova versão
4. **Registrar novo aceite** com a versão atualizada

### 6.2 Fluxo de Re-aceite

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  ⚠️ Atualizamos nossos Termos de Uso                       │
│                                                             │
│  Fizemos alterações importantes nos nossos termos.         │
│  Por favor, revise e aceite para continuar usando          │
│  o AirGate.                                                 │
│                                                             │
│  [Ver alterações] [Ler termos completos]                   │
│                                                             │
│  ☑️ Li e concordo com os novos Termos de Uso               │
│                                                             │
│           ┌─────────────────────────┐                      │
│           │       CONTINUAR         │                      │
│           └─────────────────────────┘                      │
│                                                             │
│  Não concorda? Você pode [cancelar sua conta] sem multa.   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 7. Documentos e URLs

### 7.1 Estrutura de URLs Sugerida

| Documento | URL |
|-----------|-----|
| Termos de Uso | https://airgate.app/termos-de-uso |
| Política de Privacidade | https://airgate.app/privacidade |
| Contrato Completo (PDF) | https://airgate.app/contrato |
| Termo de Consentimento Biométrico | https://airgate.app/consentimento-biometrico |

### 7.2 Versionamento

Manter histórico de versões acessível:

- https://airgate.app/termos-de-uso (sempre a versão atual)
- https://airgate.app/termos-de-uso/v1.0 (versão específica)
- https://airgate.app/termos-de-uso/historico (lista de versões)

---

## 8. Checklist de Implementação

### 8.1 Cadastro

- [ ] Checkbox de aceite obrigatório (desmarcado por padrão)
- [ ] Links para Termos e Privacidade funcionando
- [ ] Botão só habilita após marcar checkbox
- [ ] Log de aceite sendo gravado com todos os campos
- [ ] Versão do documento registrada

### 8.2 Contratação de Plano

- [ ] Resumo claro de valores antes do aceite
- [ ] Link para contrato completo
- [ ] Checkbox de aceite do contrato
- [ ] Checkbox separado para marketing (opcional)
- [ ] Log de aceite do contrato

### 8.3 Biometria de Hóspede

- [ ] Tela específica e destacada para consentimento
- [ ] Alternativa (QR Code) claramente visível
- [ ] Checkbox específico para biometria
- [ ] Link para termo completo
- [ ] Log de consentimento com data de exclusão prevista

### 8.4 Atualização de Termos

- [ ] Sistema de versionamento implementado
- [ ] Notificação por e-mail configurada
- [ ] Banner de re-aceite no painel
- [ ] Histórico de versões acessível

---

## 9. Modelo de E-mail — Atualização de Termos

```
Assunto: Atualizamos nossos Termos de Uso — Ação necessária

Olá, [NOME]!

Atualizamos nossos Termos de Uso e Política de Privacidade. 
As principais mudanças são:

• [Resumo da mudança 1]
• [Resumo da mudança 2]
• [Resumo da mudança 3]

📄 Leia os novos termos: [LINK]

Os novos termos entram em vigor em 30 dias (DD/MM/AAAA). 
Para continuar usando o AirGate, acesse seu painel e aceite 
os novos termos.

Não concorda? Você pode cancelar sua conta sem multa até a 
data de vigência dos novos termos.

Dúvidas? Responda este e-mail ou fale conosco pelo WhatsApp.

Abraços,
Equipe AirGate

---
RIDE ROBOTICS LTDA. | CNPJ 39.606.333/0001-02
Rua Jerônimo Coelho, 78 — Joinville/SC
https://airgate.app
```

---

## 10. Considerações Jurídicas

### 10.1 Validade do Click-wrap

O aceite via click-wrap é **juridicamente válido** no Brasil quando:

1. ✅ O usuário realiza ação afirmativa (marcar checkbox, clicar botão)
2. ✅ Os termos estão acessíveis antes do aceite
3. ✅ O texto é legível e compreensível
4. ✅ Há registro do aceite (data, hora, versão, IP)
5. ✅ O usuário pode recusar (mesmo que isso impeça o cadastro)

### 10.2 Referências Legais

- **Código Civil** (Lei nº 10.406/2002), Art. 107: Não exige forma especial para contratos, salvo exceções
- **Marco Civil da Internet** (Lei nº 12.965/2014), Art. 7º, VI: Termos devem conter informações claras
- **LGPD** (Lei nº 13.709/2018), Art. 8º: Consentimento deve ser fornecido por escrito ou outro meio que demonstre manifestação de vontade
- **CDC** (Lei nº 8.078/1990), Art. 46: Cláusulas devem ser redigidas de forma clara

---

*Documento interno — Guia de implementação para equipe de produto e desenvolvimento.*
