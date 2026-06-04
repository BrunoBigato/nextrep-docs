---
layout: default
title: Política de Privacidade — RankForge
---

# Política de Privacidade

**Última atualização: 28 de maio de 2026**

Esta Política de Privacidade descreve como o aplicativo **RankForge** ("RankForge", "nós", "nosso") coleta, usa, armazena e compartilha informações pessoais dos usuários ("você"), em conformidade com a **Lei Geral de Proteção de Dados Pessoais (LGPD — Lei nº 13.709/2018)**.

Ao usar o RankForge, você concorda com as práticas descritas neste documento.

---

## 1. Controlador dos dados

O controlador responsável pelo tratamento dos seus dados pessoais é:

- **Bruno Patrocínio** (Pessoa Física)
- E-mail de contato (LGPD/DPO): **rankforge.app@gmail.com**

---

## 2. Dados que coletamos

### 2.1 Dados de cadastro
- **E-mail e senha** (criptografada): para autenticação. Senhas nunca são armazenadas em texto puro.
- **Nome do Hunter** (opcional): apelido escolhido por você dentro do app.
- **Login via Google** (opcional): se você optar por entrar com sua conta Google, recebemos seu e-mail, nome e foto de perfil via OAuth, conforme escopos solicitados.

### 2.2 Dados de treino
- Ciclos, divisões de treino, exercícios cadastrados, séries executadas, cargas levantadas, métodos de progressão, histórico de execuções, recordes pessoais (PRs).
- Estes dados são gerados por você dentro do app e armazenados localmente no seu dispositivo + sincronizados com nosso servidor (se autenticado).

### 2.3 Dados de gamificação
- Nível, rank, atributos (POWER, VOLUME, DENSITY, etc.), títulos conquistados, streak de treinos.
- Esses dados são derivados da sua atividade de treino.

### 2.4 Dados de uso e diagnóstico (Sentry)
- Quando o aplicativo apresenta um erro, coletamos:
  - Stack trace técnico do erro
  - Modelo do dispositivo, versão do sistema operacional, versão do app
  - Identificador anônimo do usuário (apenas o `user_id` interno, sem e-mail ou nome)
- **Não coletamos** localização, contatos, fotos, ou qualquer dado fora do escopo de funcionamento do app.

### 2.5 Dados de assinatura (Pro)
- Status da sua assinatura (Pro/Free), plano contratado, datas de início/expiração.
- **Não armazenamos** dados de cartão de crédito ou meios de pagamento. Toda transação financeira é processada pelo Google Play e segue as políticas dele.

### 2.6 Importação de PDF (System Scan — feature Pro)
- Quando você importa um PDF de ficha de treino, o conteúdo do PDF é enviado temporariamente para a **Anthropic** (provedor da IA Claude) para extração estruturada dos exercícios.
- O conteúdo do PDF **não é armazenado** após o processamento. Apenas os dados extraídos (exercícios, séries, cargas) ficam salvos na sua conta.

---

## 3. Como usamos seus dados

Usamos os dados coletados para:

- Permitir login, autenticação e recuperação de conta.
- Armazenar e sincronizar seus treinos entre dispositivos.
- Calcular progressão de carga, sugestões de treino e métricas de evolução.
- Gerenciar assinaturas Pro e validar entitlements.
- Identificar e corrigir erros técnicos do aplicativo.
- Cumprir obrigações legais e regulatórias.

**Não usamos** seus dados para publicidade, perfilamento comercial ou venda a terceiros.

---

## 4. Base legal (LGPD Art. 7)

O tratamento dos seus dados pessoais está fundamentado nas seguintes bases legais:

| Dado | Base legal |
|------|------------|
| Cadastro, login, treino | Execução de contrato (Art. 7, V) |
| Crash reports | Legítimo interesse — melhoria do serviço (Art. 7, IX) |
| Assinatura Pro | Execução de contrato (Art. 7, V) |
| PDF import | Consentimento (Art. 7, I) — você ativa a feature manualmente |
| Login Google | Consentimento (Art. 7, I) — opcional |

---

## 5. Compartilhamento com terceiros

Compartilhamos dados estritamente necessários com os seguintes operadores:

| Operador | Finalidade | Dados | Localização |
|----------|------------|-------|-------------|
| **Supabase Inc.** | Backend, autenticação e banco de dados | Cadastro + treinos | EUA / União Europeia |
| **Anthropic PBC** | Processamento de PDF via IA (apenas Pro) | Conteúdo do PDF importado | EUA |
| **Sentry (Functional Software, Inc.)** | Relatório de erros | Stack trace + ID anônimo | EUA |
| **Google LLC** | Login Google (opcional) + pagamentos via Google Play | E-mail, nome, status de assinatura | EUA |
| **RevenueCat, Inc.** | Gestão de entitlements de assinatura | ID de usuário + status Pro | EUA |

**Não vendemos, alugamos ou cedemos seus dados** para qualquer outra empresa.

### 5.1 Transferência internacional
Alguns operadores acima armazenam dados fora do Brasil. Você consente expressamente com essa transferência ao usar o RankForge, conforme Art. 33 da LGPD. Todos os operadores listados possuem políticas próprias de proteção compatíveis com a LGPD ou GDPR.

---

## 6. Seus direitos (LGPD Art. 18)

Você tem o direito de, a qualquer momento:

1. **Confirmar** a existência de tratamento dos seus dados
2. **Acessar** os dados que temos sobre você
3. **Corrigir** dados incompletos, inexatos ou desatualizados
4. **Anonimizar, bloquear ou eliminar** dados desnecessários
5. **Solicitar portabilidade** dos seus dados para outro fornecedor
6. **Eliminar** dados tratados com base em consentimento
7. **Obter informação** sobre com quem compartilhamos seus dados
8. **Revogar consentimento** a qualquer momento

### Como exercer
- **Excluir conta**: dentro do app, em *Configurações → Excluir conta* (deleta toda sua conta e dados em até 30 dias).
- **Demais direitos**: envie um e-mail para **rankforge.app@gmail.com** com o assunto "LGPD — [seu pedido]". Respondemos em até 15 dias úteis.

---

## 7. Retenção de dados

- Seus dados ficam armazenados enquanto sua conta estiver ativa.
- Ao solicitar exclusão de conta (via app ou e-mail), removemos todos os dados pessoais em até **30 dias**.
- Dados anonimizados (sem possibilidade de identificação) podem ser mantidos para fins estatísticos.
- Crash reports do Sentry são automaticamente apagados após 90 dias.

---

## 8. Segurança

Adotamos medidas técnicas e administrativas para proteger seus dados:

- Senhas armazenadas com hash seguro (bcrypt via Supabase Auth).
- Conexões protegidas por TLS/HTTPS.
- Row-Level Security (RLS) no banco: nenhum usuário acessa dados de outro.
- Tokens de autenticação armazenados em armazenamento seguro do dispositivo (Keychain/Keystore).
- Acesso restrito a logs internos apenas para diagnóstico técnico.

Apesar dos cuidados, nenhum sistema é 100% imune. Em caso de incidente de segurança que possa afetar você, notificaremos a Autoridade Nacional de Proteção de Dados (ANPD) e os usuários impactados, conforme Art. 48 da LGPD.

---

## 9. Crianças e adolescentes

O RankForge não é destinado a menores de **13 anos**. Não coletamos intencionalmente dados de crianças. Se você é responsável legal e identificou cadastro indevido, entre em contato em **rankforge.app@gmail.com** para remoção imediata.

---

## 10. Cookies e rastreadores

O RankForge é um aplicativo móvel e **não utiliza cookies de navegador**. Não usamos pixels de rastreamento, fingerprinting ou ferramentas de publicidade comportamental.

---

## 11. Alterações nesta política

Esta política pode ser atualizada periodicamente. Mudanças relevantes serão comunicadas dentro do aplicativo ou por e-mail. A data da última atualização sempre estará no topo deste documento.

---

## 12. Contato

Dúvidas, reclamações ou solicitações relacionadas a privacidade:

**E-mail**: rankforge.app@gmail.com
**Assunto sugerido**: "LGPD — [descrição]"

---

[← Voltar](./)
