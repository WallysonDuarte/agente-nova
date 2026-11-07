---
name: desenho-de-atividade
description: Produzir o documento que antecede a implementacao: objetivo, decisoes tecnicas, arquivos afetados, checklist e casos de uso.
---

# Desenho de atividade (blueprint)

## Quando usar

Antes de **qualquer** implementacao. Atividade sem desenho nao esta autorizada a comecar.

## Estrutura do documento

```markdown
# Desenho — <titulo da atividade>

Data: <data>
Objetivo: <uma frase: que problema isso resolve, para quem>

## O que sera feito
<descricao objetiva do escopo>

## Fora de escopo
<o que explicitamente NAO sera feito nesta atividade>

## Decisoes tecnicas
| Decisao | Alternativa descartada | Por que |
|---|---|---|

## Arquivos e componentes afetados
- [ ] <caminho relativo> — criar | alterar | remover

## Criterios de aceite
1. Dado <contexto>, quando <acao>, entao <resultado observavel>

## Casos de uso (minimo 5)
1. Caminho feliz
2. Entrada vazia / campo obrigatorio ausente
3. Duplicidade / conflito
4. Valor no limite (minimo, maximo, estouro)
5. Falha externa (rede, servico indisponivel, permissao negada)

## Riscos
<o que pode dar errado e qual o plano>

## Resultado (preenchido no fim)
<resultado, commits, licoes>
```

## Como escrever criterio de aceite

Formato: **Dado / Quando / Entao**, com resultado observavel.

| Ruim | Bom |
|---|---|
| "Tela deve ser rapida" | "Dado 10 mil registros, quando abrir a listagem, entao a primeira pagina renderiza em menos de 2 s" |
| "Validar o formulario" | "Dado documento com digito verificador invalido, quando enviar, entao exibe erro ao lado do campo e nao chama a API" |
| "Deve ser seguro" | "Dado usuario sem permissao administrativa, quando acessar a rota de usuarios, entao recebe 403 e nao ve a listagem" |

Criterio que ninguem consegue verificar por observacao nao e criterio.

## Casos de uso: a lista minima

Para **todo** fluxo, especifique:

1. **Caminho feliz** — tudo certo, resultado esperado.
2. **Entrada invalida** — campo obrigatorio vazio, formato errado, caractere inesperado.
3. **Conflito** — registro duplicado, recurso ja usado, estado incompativel.
4. **Limite** — zero, um, maximo permitido, um acima do maximo.
5. **Falha externa** — servico fora, tempo esgotado, permissao negada, pagamento recusado.

Se o fluxo mexe em dinheiro, estado ou dado de terceiro, acrescente:

6. **Repeticao** — mesma operacao enviada duas vezes (duplo clique, nova tentativa).
7. **Concorrencia** — duas pessoas agindo sobre o mesmo registro ao mesmo tempo.

## Ambiguidade

Quando o pedido admite duas leituras que levam a trabalhos diferentes, **nao escolha em silencio**.
Registre no desenho:

```
Premissa adotada: <interpretacao escolhida>
Alternativa: <outra leitura>
Impacto se a premissa estiver errada: <retrabalho estimado>
```

E declare a premissa na comunicacao. Isso permite correcao antes do custo.

## Checklist

- [ ] Objetivo em uma frase, com o problema e o beneficiario
- [ ] Escopo e fora-de-escopo escritos
- [ ] Decisoes tecnicas com alternativa descartada e motivo
- [ ] Lista de arquivos/componentes afetados
- [ ] Criterios de aceite verificaveis no formato Dado/Quando/Entao
- [ ] Minimo 5 casos de uso, com erro e limite
- [ ] Riscos e plano
- [ ] Documento atualizado no fim com resultado e licoes

## Pronto quando

Quem for implementar consegue comecar sem fazer nenhuma pergunta, e quem for validar sabe
exatamente o que medir.
