---
name: priorizacao
description: Ordenar a fila por valor e custo com justificativa escrita, usando classificacao de obrigatoriedade e matriz impacto/esforco.
---

# Priorizacao de fila

## Quando usar

Fila com mais itens do que capacidade — ou seja, sempre.

## Dois instrumentos

### 1. Classificacao de obrigatoriedade

- **Obrigatorio** — sem isso a entrega nao tem sentido. Se cair, nao entrega.
- **Importante** — doloroso sem, mas existe contorno aceitavel.
- **Desejavel** — melhora, entra se sobrar capacidade.
- **Fora** — decidido que **nao** sera feito agora. Registrar e tao importante quanto o resto:
  evita a pergunta voltar toda semana.

Regra: no maximo 60% da capacidade comprometida com obrigatorios. Fila 100% obrigatoria significa
que nada e obrigatorio de verdade.

### 2. Matriz impacto x esforco

```
             esforco baixo        esforco alto
impacto    +------------------+------------------+
  alto     |  FAZER AGORA     |  PLANEJAR        |
           +------------------+------------------+
impacto    |  ENCAIXAR        |  NAO FAZER       |
  baixo    |                  |                  |
           +------------------+------------------+
```

Item de impacto baixo e esforco alto nao vai para o fim da fila: vai para **fora**, com a decisao
registrada.

## Valor: como estimar sem inventar

Combine o que der para medir:

- **Alcance** — quantas pessoas sao afetadas por periodo
- **Intensidade** — quanto muda para cada uma (bloqueio, atrito, conveniencia)
- **Confianca** — qualidade da evidencia (dado medido > relato recorrente > suposicao)
- **Esforco** — estimativa relativa da equipe

Prioridade cresce com alcance x intensidade x confianca, e cai com esforco. Nao finja precisao:
uma ordenacao por faixas (alta/media/baixa) com justificativa escrita vale mais que um numero
inventado com duas casas decimais.

## Correcao de defeito entra na frente?

| Situacao | Posicao |
|---|---|
| Perda ou corrupcao de dado | imediata, interrompe o que estiver em curso |
| Vulnerabilidade exploravel | imediata |
| Fluxo central bloqueado para todos | imediata |
| Fluxo central bloqueado para alguns | topo da fila |
| Fluxo secundario com contorno | fila normal, classificado |
| Incomodo cosmetico | fila normal, provavelmente desejavel |

## Registro de decisao

Para cada mudanca de prioridade:

```
Item: <titulo>
De: <posicao anterior>   Para: <nova posicao>
Motivo: <evidencia>
O que sai do lugar: <item deslocado>
```

Priorizacao sem dizer **o que sai** nao e priorizacao, e lista de desejos.

## Checklist

- [ ] Todo item classificado por obrigatoriedade
- [ ] Obrigatorios dentro de 60% da capacidade
- [ ] Impacto e esforco estimados, com nivel de confianca
- [ ] Itens descartados registrados como "fora", nao esquecidos no fim
- [ ] Toda mudanca de prioridade diz o que foi deslocado
- [ ] Justificativa escrita, nao verbal

## Pronto quando

Qualquer pessoa olha a fila e entende por que o primeiro item e o primeiro — sem precisar perguntar.
