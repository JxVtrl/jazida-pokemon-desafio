# 🧪 Desafio Técnico - Jazida Pokémon

## 🌐 Ambientes de Deploy

- **Frontend Produção:** [https://jazida.pokemon.majorssolutions.com.br](https://jazida.pokemon.majorssolutions.com.br)
- **Backend Produção (API):** [https://jazida.api.majorssolutions.com.br](https://jazida.api.majorssolutions.com.br)
- **Documentação da API:** [https://jazida.api.majorssolutions.com.br/api-docs](https://jazida.api.majorssolutions.com.br/api-docs)

**Variável de ambiente do frontend para produção:**
```env
NEXT_PUBLIC_API_URL=https://jazida.api.majorssolutions.com.br
```

Este repositório contém a estrutura principal do desafio técnico para a vaga de Desenvolvedor(a) Fullstack no Jazida. A aplicação é dividida em dois submódulos Git:

- [`frontend/`](./frontend): Interface inspirada no HUD clássico das batalhas de Pokémon.
- [`backend/`](./backend): API REST em Node.js com lógica de batalhas e gestão de Pokémons.

---

## 📦 Estrutura

```bash
jazida-pokemon-desafio/
├── backend/     # Submódulo: API Express com lógica de batalha
├── frontend/    # Submódulo: UI em Next.js com estilo retrô Pokémon
└── README.md
```

## 🚀 Clonando o projeto com submódulos

Para clonar o repositório com os submódulos já incluídos:

```bash
git clone --recurse-submodules git@github.com:JxVtrl/jazida-pokemon-desafio.git
cd jazida-pokemon-desafio
```

Se você já clonou sem `--recurse-submodules`, pode rodar:

```bash
git submodule update --init --recursive
```

## 📂 Sobre cada subprojeto

### 🔁 Backend (`/backend`)
- **Node.js + Express**
- **Socket.IO** para efeitos em tempo real
- **Banco de dados** à sua escolha (PostgreSQL ou SQLite recomendados)
- **Lógica probabilística** de batalhas baseada em níveis

Veja mais detalhes no [`/backend/README.md`](./backend/README.md)

### 🎮 Frontend (`/frontend`)
- **Next.js + Tailwind CSS**
- **Layout estilo GameBoy** (HUD retrô de batalha)
- **Simulação visual** da batalha com suspense
- **Integração** com a API e com Socket.IO

Mais informações no [`/frontend/README.md`](./frontend/README.md)

## 🧪 Testes e extras

Este projeto pode incluir:

- ✅ **Testes automatizados** (unitários e/ou integração)
- ✅ **CI/CD** com GitHub Actions
- ✅ **Deploy remoto** (ex: VPS pessoal)
- ✅ **Documentação da API** com Swagger ou equivalente

## 🧠 Objetivo do Desafio

Implementar um **CRUD de Pokémons** com os tipos `charizard`, `mewtwo` ou `pikachu`, e uma **lógica de batalhas** baseada na chance proporcional ao nível de cada um. O frontend simula visualmente a batalha com uma experiência inspirada nos jogos clássicos.

### 📋 Funcionalidades Principais

#### 1. CRUD de Pokémons
- **Create**: Criar novo Pokémon
- **Read**: Visualizar Pokémon específico
- **Update**: Atualizar dados do Pokémon
- **Delete**: Remover Pokémon
- **List**: Listar todos os Pokémons

**Campos obrigatórios:**
- `tipo` (charizard, mewtwo, pikachu)
- `treinador` (nome do treinador)
- `nivel` (nível do Pokémon)

#### 2. Sistema de Batalhas
- **Seleção aleatória** do vencedor baseada no nível
- **Probabilidade**: Pokémon de nível superior tem maior chance de vitória
  - Exemplo: nível 2 vs nível 1 → 66% de chance para o nível 2
- **Evolução**: Vencedor ganha +1 nível
- **Penalidade**: Perdedor perde -1 nível (deletado se chegar a 0)

## 🧑‍💻 Autor

Desenvolvido por **João Vinicius Vitral** para o desafio técnico do Jazida.

- **GitHub**: [@JxVtrl](https://github.com/JxVtrl)
- **LinkedIn**: [João Vinicius Vitral](https://www.linkedin.com/in/joao-vinicius-vitral/)

---

<div align="center">

**Gotta code 'em all!** 🎮⚡

</div>