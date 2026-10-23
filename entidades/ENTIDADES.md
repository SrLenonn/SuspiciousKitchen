# Entidades do jogo — Suspicious Kitchen

**Integrantes:** Iuri Castro e Kaique Fernandes

**Checkpoint 2 · Programação para Jogos I **

## 1. Entidades

O que se move, muda de estado ou reage a algo? Uma por linha.

- Jogador
- Cliente
- Humano herda de Cliente
- Monstro herda de Cliente
- Pedidos
- Receitas
- Ingredientes
- Comidas
- Ferramentas de cozinha

## 2. Propriedades

O que cada entidade sabe sobre si?

| Entidade | Propriedades |
|---|---|
| Jogador | Estresse, Inventário |
| cliente | Nome, Perfil, Restrições, Espécie, Características, Preferências, Nível, Estado |
| Pedidos | Nome, Itens Solicitados, Status, Nível |
| Receitas | Nome, Modo, Nível,Igredientes |
| Ingrediente | Nome, Categoria, Características, Qualidade |
| Comidas | Nome, Etapa, Receita, Qualidade |
| Estações | Nome, Função, Disponibilidade |

## 3. Comportamentos

O que cada entidade faz a cada quadro?

| Entidade | Comportamentos |
|---|---|
| Jogador | Interagir com Clientes, Anota Pedidos, Entrega Comida, Atualiza Estresse, Inventário |
| Cliente | Fazer Pedido, Avalia Atendimento, Encerrar atendimento |
| Pedidos | Atualiza Status, Verifica Conclusão |
| Receitas | Consulta Ingredientes, Consulta Etapa, Valida o Preparo |
| Ingredientes | Nada |
| Comidas | Adiciona Ingredientes, Registra Etapa, Valida Qualidade |
| Estações | Seleção, Ação, Verifica Compatibilidade, Atualiza Qualidade do Ingrediente | 


## 4. Colisões

O que colide com o quê? A reação é igual para todo par?

| Quem | Com quem | O que acontece |
|---|---|---|
| Igredientes | Estações | Trata o igrediente |

## 5. Comunicação

Uma entidade aciona ou lê a outra diretamente, ou por um terceiro (o jogo, o mundo, um gerenciador)?

- Jogador → Cliente : Direto
- Jogador → Comida : Direto
- Cliente → Pedido: Direto
- Pedido → Comida: Direto
- Pedido → Receita: Direto
- Rceita → Comida: Direto
- Receita → Ingrediente: Direto
- Comida → Ingrediente: Direto
- Ferramenta → Ingrediente: Direto

## 6. Falsas entidades

Algo parece entidade, mas não se atualiza sozinho (placar, cenário, som, câmera)?

- Cenários do Jogo: Balcão de atendimento, Cozinha
- Manuais de Interação: Manual de Investigação, Livro de Receitas
- Barras de Status: Barra de Stress

## 7. Repetições

Duas ou mais entidades repetem o mesmo comportamento? Qual, e em quais?

- Nada repete
