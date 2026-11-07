---
name: metricas-de-produto
description: Definir e acompanhar metricas de aquisicao, ativacao, retencao, receita e indicacao, ligando cada entrega a um indicador.
---

# Metricas de produto

## Quando usar

Ao definir o que medir numa entrega, montar painel de acompanhamento ou avaliar se uma entrega
funcionou.

## As cinco familias

| Familia | Pergunta | Indicadores |
|---|---|---|
| Aquisicao | chegam? | visitantes unicos, taxa de cadastro, custo de aquisicao |
| Ativacao | entendem? | conclusao do primeiro uso, tempo ate o primeiro valor |
| Retencao | voltam? | ativos diarios sobre mensais, evasao, analise por coorte |
| Receita | pagam? | receita recorrente, receita media por usuario, valor no ciclo de vida, conversao gratuito-pago |
| Indicacao | recomendam? | indice de recomendacao, coeficiente viral, avaliacoes |

## Uma metrica por entrega

Toda entrega declara, **antes** de comecar, qual indicador deve se mover e em quanto:

```
Entrega: <titulo>
Indicador: <nome>
Valor atual: <numero medido hoje>
Meta: <numero> em <prazo>
Como medir: <fonte do dado>
```

Sem valor atual medido, nao existe meta — existe palpite. Se nao da para medir hoje, a primeira
entrega e **instrumentar a medicao**.

## Analise por coorte

Metrica agregada esconde o efeito da mudanca: usuarios antigos diluem o comportamento dos novos.
Compare grupos pela data de entrada — so assim se ve se a alteracao de hoje melhorou a retencao de
quem entrou depois dela.

## Armadilhas

- **Metrica de vanidade.** Total acumulado sempre sobe e nao informa nada. Prefira taxa e periodo.
- **Media escondendo distribuicao.** Tempo medio de resposta de 200 ms com percentil 95 em 8 s e
  um sistema lento. Olhe percentis.
- **Correlacao tratada como causa.** Receita subiu na semana da entrega **e** da campanha. Separe
  por grupo ou aceite que nao da para atribuir.
- **Denominador movel.** Mudar a definicao de "ativo" no meio do acompanhamento invalida a serie.
- **Fuso horario.** Dado agregado em tempo universal exibido como data local desloca o dia e faz a
  serie parecer errada.

## Ciclo de acompanhamento

- **Semanal:** indicadores do fluxo central; desvio grande merece investigacao imediata.
- **Mensal:** relatorio comparando mes anterior e mesmo mes do ano anterior, com leitura do que
  mudou e proximos passos.
- **Trimestral:** revisao dos objetivos — a meta ainda e a certa?

Relatorio sempre responde tres perguntas: o que mudou, por que mudou, o que fazer a respeito.

## Checklist

- [ ] Indicador declarado antes da entrega, com valor atual medido
- [ ] Fonte do dado identificada e acessivel
- [ ] Analise por coorte quando a mudanca afeta comportamento ao longo do tempo
- [ ] Percentis, nao apenas media, para tempo e latencia
- [ ] Definicoes estaveis (ativo, convertido, evadido) documentadas
- [ ] Relatorio com leitura e acao, nao apenas numeros

## Pronto quando

Cada entrega tem um indicador com valor antes e depois, e o relatorio diz o que fazer com o
resultado.
