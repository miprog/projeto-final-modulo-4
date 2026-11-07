# ADR - Decisao de refatoracao

## Decisao
Usar o padrao Strategy para descontos em vez de if/else dentro do PedidoService.

## Por que
- Cada desconto fica em uma classe separada
- Facilita testar cada regra sozinha
- Para criar um desconto novo, nao preciso mexer no codigo que ja funciona

## Consequencia
PedidoService so calcula o valor bruto e delega o desconto para a estrategia escolhida.