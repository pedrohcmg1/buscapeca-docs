# Busca Peça · Documentação

Marketplace web de autopeças que conecta oficinas e compradores a lojas que vendem peças novas, usadas e excedentes. Uma mesma conta compra e, depois de criar a loja, também vende.

Este repositório reúne os artefatos exigidos na avaliação da disciplina **Escola de TI**. Cada artefato está exportado em PDF ou XLSX para abrir sem depender da ferramenta original.

## Planejamento

| Artefato | Arquivo | Conteúdo |
|---|---|---|
| Especificação de caso de uso | [especificacao-casos-de-uso.xlsx](planejamento/especificacao-casos-de-uso.xlsx) | User stories, modelo e uma aba por caso de uso (57 casos, BP1-2 a BP1-67) |
| Diagrama de caso de uso | [diagrama-casos-de-uso.pdf](planejamento/diagrama-casos-de-uso.pdf) | Atores e casos por área: conta, comprador, vendedor e administrador, com tabela de rastreabilidade |
| DER e Diagrama de classes | [der-e-diagrama-de-classes.pdf](planejamento/der-e-diagrama-de-classes.pdf) | 46 entidades e 44 classes, divididas em 5 módulos e geradas a partir do mesmo modelo |
| Diagrama de atividades | [diagramas-de-atividades.pdf](planejamento/diagramas-de-atividades.pdf) | 6 fluxos do MVP em UML 2 com raias: compra, criar loja, operar pedido, conta, recuperar senha e disputa |

## Pré-código

| Artefato | Arquivo | Conteúdo |
|---|---|---|
| Consolidação de ADRs | [consolidacao-adrs-v2.pdf](pre-codigo/consolidacao-adrs-v2.pdf) | 15 decisões de arquitetura (status, contexto, decisão, alternativas e consequências) e o impacto de cada uma nos demais artefatos |

## Principais decisões

- **Stack:** API REST em Java 21 com Spring Boot, MySQL 8 com Flyway e front-end em HTML, CSS e JavaScript com Bootstrap (ADR-001, 004 e 014).
- **Conta única:** toda conta nasce compradora e passa a vender ao criar a loja (ADR-007).
- **Um pedido por loja:** o carrinho multilojas vira uma compra dividida em um pedido por loja (ADR-009).
- **Pagamento fora do MVP:** pagamento, frete e retirada são combinados entre as partes (ADR-008).
- **LGPD desde o início:** aceite versionado dos termos, log de auditoria e exclusão com anonimização (ADR-013).

## Estrutura

```
.
├── README.md
├── planejamento/
│   ├── especificacao-casos-de-uso.xlsx
│   ├── diagrama-casos-de-uso.pdf
│   ├── der-e-diagrama-de-classes.pdf
│   └── diagramas-de-atividades.pdf
└── pre-codigo/
    └── consolidacao-adrs-v2.pdf
```
