# Mapa de Contexto

## Contextos Delimitados

- **Central de Exames**: Core Domain
- **Sistema de Faturamento**: Suporte
- **Sistema de Contabilidade**: Suporte
- **Laboratório Parceiro**: Genérico
- **Laboratório Conveniado**: Genérico
- **Ferramenta de Assinatura Digital**: Genérico

## Integrações

- **Central de Exames** <-> **Sistema de Faturamento**: Shared Kernel
- **Central de Exames** <-> **Sistema de Contabilidade**: Shared Kernel
- **Central de Exames** <-> **Laboratório Parceiro**: Parceria
- **Central de Exames** <-> **Laboratório Conveniado**: Conformista
- **Central de Exames** <-> **Ferramenta de Assinatura Digital**: Camada anticorrupção

## Fluxo de Dados

- **Downstream**: Sistema de Faturamento, Sistema de Contabilidade, Laboratório Parceiro, Laboratório Conveniado, Ferramenta de Assinatura Digital
- **Upstream**: Central de Exames
