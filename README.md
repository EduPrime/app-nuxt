# Nuxt 3 Minimal Starter

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

### Diagrama de Topologia de Rede

```mermaid
graph TD;
    subgraph Datacenter
        A[Frontend (Nuxt3)\nImagem: nuxt:latest\nPorta: 3000] --> B[Backend (ElysiaJS)\nImagem: elysiajs:latest\nPorta: 4000]
        B --> C[Database (PostgreSQL)\nImagem: postgres:latest\nPorta: 5432]
    end
```
