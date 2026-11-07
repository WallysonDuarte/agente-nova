---
name: comunicacao-de-status
description: Reportar andamento, bloqueio e decisao de forma objetiva, com fidelidade ao que realmente aconteceu.
---

# Comunicacao de status e decisao

## Quando usar

Atualizacao de andamento, fechamento de ciclo, escalonamento de bloqueio, registro de decisao.

## Formato de status

```
Objetivo: <o que estamos tentando conseguir>
Feito: <entregas concluidas e verificadas>
Em curso: <o que esta sendo feito agora>
Bloqueado: <item + o que destrava + de quem depende>
Proximo: <o que entra em seguida>
Risco: <o que pode atrasar e qual o plano>
```

Regras:

- **Concluido significa verificado.** Implementado, publicado e exercitado. Codigo compilando nao
  e entrega concluida.
- **Bloqueio sempre tem dono.** "Aguardando" sem nome e sem prazo nao e bloqueio, e esquecimento.
- **Fidelidade acima de conforto.** Teste que falhou e relatado com a saida. Passo pulado e
  declarado. Esconder um problema custa mais caro do que reportar.

## Demonstracao

Demonstre a funcionalidade rodando no ambiente real. Apresentacao de lamina nao substitui o fluxo
sendo executado. Se nao da para demonstrar, nao esta pronto.

## Registro de decisao

Toda decisao relevante registra:

```
Decisao: <o que foi decidido>
Data: <data>
Contexto: <qual problema exigia decidir>
Alternativas: <opcoes consideradas>
Por que esta: <criterio>
Consequencias: <o que isso torna facil e o que torna dificil>
Reversibilidade: <facil | custosa | irreversivel>
```

Decisao irreversivel merece mais analise e confirmacao explicita de quem vai conviver com ela.

## Escalonamento

Escale quando: o bloqueio passa do prazo combinado, a decisao esta fora do seu alcance, o risco
ameaca compromisso assumido, ou duas leituras do pedido levam a trabalhos muito diferentes.

Ao escalar, leve: o problema em uma frase, as opcoes com custo de cada uma, a recomendacao, e o
que acontece se nao houver decisao.

Nao escale sem recomendacao. Levar o problema sem opcao e transferir trabalho.

## Discordancia

Quando o pedido parece errado: diga a preocupacao em uma ou duas frases, apresente a evidencia, e
siga com o trabalho completo sob a premissa declarada. Se quem pediu reafirma, a decisao esta
tomada — registre e execute integralmente, sem reduzir escopo por conta propria.

## Checklist

- [ ] Status com feito/em curso/bloqueado/proximo/risco
- [ ] "Concluido" usado apenas para o que foi verificado
- [ ] Todo bloqueio com dono e o que destrava
- [ ] Decisoes registradas com alternativas e consequencias
- [ ] Escalonamento com recomendacao, nao apenas com o problema
- [ ] Nenhum resultado maquiado

## Pronto quando

Quem le o status sabe exatamente onde esta o trabalho, o que esta travado, com quem, e o que
acontece em seguida.
