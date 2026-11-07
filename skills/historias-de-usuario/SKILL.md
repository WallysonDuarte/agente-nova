---
name: historias-de-usuario
description: Escrever historias no formato persona-acao-beneficio, quebrar epicos e definir a condicao de pronto compartilhada.
---

# Historias de usuario e refinamento

## Quando usar

Ao transformar uma necessidade em itens de fila executaveis.

## Formato

```
Como <persona concreta>
quero <acao observavel>
para <beneficio mensuravel>
```

Persona concreta, nao "usuario". `Como administrador financeiro` diz mais que `Como usuario`.
Beneficio mensuravel, nao "para melhorar a experiencia".

## Quebra de epico

Um epico cabe em um trimestre; uma historia cabe em uma entrega; uma tarefa cabe em uma sessao de
trabalho.

Divida por **fatia vertical** (cada fatia entrega valor de ponta a ponta), nunca por camada
tecnica:

| Divisao ruim (horizontal) | Divisao boa (vertical) |
|---|---|
| "Criar tabela de pedidos" | "Cliente consegue registrar um pedido e ve-lo na lista" |
| "Criar API de pedidos" | "Cliente consegue cancelar um pedido ainda nao pago" |
| "Criar tela de pedidos" | "Administrador consegue filtrar pedidos por situacao" |

A divisao horizontal produz tres itens em que nenhum, isoladamente, funciona.

## Tecnicas de quebra

- Por regra de negocio (com desconto / sem desconto)
- Por tipo de dado (apenas texto primeiro, anexos depois)
- Por operacao (ler primeiro, escrever depois)
- Por perfil (usuario comum primeiro, administrador depois)
- Pelo caminho feliz primeiro, tratamento de erro como item seguinte **explicito** — nunca
  implicito

## Condicao de pronto (compartilhada)

Vale para toda historia, nao se repete em cada uma:

- [ ] Implementado e compilando sem erro
- [ ] Criterios de aceite verificados um por um
- [ ] Casos de erro tratados com mensagem util
- [ ] Funciona nos tres tamanhos de tela de referencia
- [ ] Publicado no ambiente real e exercitado ali
- [ ] Sem regressao no fluxo principal
- [ ] Registro da atividade atualizado

## Estimativa

Estimativa relativa (comparacao entre itens) e mais confiavel que estimativa em horas. Item que
nao se consegue estimar nao esta refinado: falta informacao, nao coragem.

Sinais de item nao refinado:
- Ninguem sabe dizer o que acontece no caso de erro
- Depende de decisao que ainda nao foi tomada
- Depende de outro item que ainda nao existe na fila
- A estimativa varia mais de 3x entre quem estima

## Checklist

- [ ] Persona concreta, acao observavel, beneficio mensuravel
- [ ] Fatia vertical: entrega valor isoladamente
- [ ] Criterios de aceite verificaveis
- [ ] Dependencias explicitas e presentes na fila
- [ ] Caso de erro como criterio ou como item proprio declarado
- [ ] Estimavel

## Pronto quando

A historia cabe em uma entrega, funciona por si, e qualquer pessoa da equipe explica como validar.
