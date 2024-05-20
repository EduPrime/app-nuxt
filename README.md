# EduPrime - Digital Class Diary System

EduPrime é um sistema de diário de classe digital desenvolvido para escolas municipais públicas. Este projeto é uma iniciativa de código aberto para fornecer uma solução eficiente e acessível para o gerenciamento de registros acadêmicos.

## Sobre o Projeto

EduPrime é construído usando as seguintes tecnologias:
- **Frontend**: Nuxt 3 com Vuetify 3
- **Backend**: ElysiaJS
- **Banco de Dados**: PostgreSQL
- **Outras Ferramentas**: TypeScript, Composition API,  Sentry

## Documentação

Para saber mais sobre o Nuxt 3, consulte a [documentação oficial](https://nuxt.com/docs/getting-started/introduction).

## Diagrama de Topologia de Rede
+-----------------+           +----------------+           +-----------------+
|                 |           |                |           |                 |
|    Frontend     | --------> |    Backend     | --------> |    PostgreSQL   |
| (Nuxt + Vuetify)|           | (Bun +         |           |                 |
|                 |           |   ElysiaJS)    |           |                 |
+-----------------+           +----------------+           +-----------------+

## Instalação

### Requisitos

- Node.js
- Bun (opcional, mas recomendado)
- Docker (para o ambiente de desenvolvimento completo)

### Passos para Instalação

1. **Clone o Repositório**

```bash
git clone https://github.com/seu-usuario/eduprime.git
cd eduprime
```

2. **Instale as Dependências**

```bash
bun install
```

3. **Configuração do Ambiente**

Crie um arquivo `.env` na raiz do projeto e adicione as seguintes variáveis de ambiente:

```env
DATABASE_URL=postgres://usuario:senha@localhost:5432/eduprime
```

4. **Inicie a Aplicação**

```bash
bun dev
```

## Scripts Disponíveis

- `bun dev`: Inicia o servidor de desenvolvimento
- `bun build`: Compila a aplicação para produção
- `bun start`: Inicia o servidor em modo de produção
- `bun lint`: Executa o linting no código
- `bun lint:fix`: Executa o linting e corrige problemas automaticamente

## Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a Licença BSL 1.1. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

**Softagon Sistemas**

*Desenvolvendo soluções inovadoras para a educação.*

---
