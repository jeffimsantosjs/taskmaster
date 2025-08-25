# Sistema de Gestão para Confeitaria

Um sistema web completo para gestão de confeitaria com controle de estoque multi-nível, agendamento de pedidos, produção e relatórios financeiros.

## 🍰 Funcionalidades

### Gestão de Estoque
- **Matérias-Primas**: Controle de insumos com estoque mínimo e alertas
- **Receitas**: Gestão de receitas com ingredientes e rendimento
- **Produtos Finais**: Produtos compostos por receitas e embalagens
- **Embalagens**: Controle de caixas, sacolas, tags e acessórios

### Fluxo de Produção
- **Produção de Receitas**: Consome matérias-primas → gera receitas prontas
- **Produção de Produtos**: Consome receitas + embalagens → gera produtos finais
- **Validação de Estoque**: Verificação automática antes da produção

### Vendas e Pedidos
- **Pedidos Agendados**: Sistema completo com agenda e status
- **Venda Rápida (PDV)**: Interface otimizada para vendas no balcão
- **Clientes**: Cadastro com aniversários e histórico
- **Etiquetas**: Impressão térmica ou PDF para receita e cozinha

### Relatórios
- **Financeiro**: DRE, fluxo de caixa, ticket médio
- **Clientes**: Ranking, aniversariantes, frequência
- **Produtos**: Mais vendidos, margem, rotatividade
- **Estoque**: Alertas de reposição, movimentação

## 🚀 Tecnologias

### Frontend
- **Next.js 14** com App Router
- **TypeScript** para tipagem
- **Tailwind CSS** + **Radix UI** para interface
- **React Hook Form** + **Zod** para formulários
- **TanStack Query** para cache e sincronização

### Backend
- **Next.js API Routes** (REST)
- **Prisma ORM** com PostgreSQL
- **NextAuth** para autenticação
- **Serviços de produção** e **etiquetas**

### Banco de Dados
- **PostgreSQL** via Supabase (produção)
- **SQLite** para desenvolvimento local

## 📦 Instalação

### 1. Clonar o repositório
```bash
git clone <repositorio>
cd sistema-confeitaria
