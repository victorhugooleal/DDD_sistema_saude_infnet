# Artefatos DDD para o Sistema de Saúde

Este documento apresenta a modelagem baseada na abordagem Domain Driven Design (DDD) para um sistema de saúde responsável pelo registro de exames nos prontuários dos pacientes. A modelagem inclui a identificação e delimitação de contextos, determinação dos domínios e subdomínios, e a classificação dos mesmos como domínio principal, domínio genérico e/ou domínio de suporte.

## 1. Mapa de Contexto

O Mapa de Contexto ilustra as interações entre os diferentes contextos delimitados do sistema. Ele ajuda a entender como os diferentes componentes do sistema se comunicam e colaboram entre si.

![Mapa de Contexto](context-map.png)

## 2. Linguagem Ubíqua

A Linguagem Ubíqua é um conjunto de termos e definições que são usados consistentemente em todo o projeto para garantir uma comunicação clara e precisa entre todos os envolvidos. Os termos importantes para este domínio incluem:

1. **Paciente**: Indivíduo que recebe atendimento médico e realiza exames.
2. **Prontuário Eletrônico**: Registro digital contendo informações médicas do paciente.
3. **Exame**: Procedimento médico realizado para diagnosticar ou monitorar condições de saúde.
4. **Laudo**: Documento médico que contém os resultados e interpretações dos exames.
5. **Laboratório Central**: Entidade responsável pela realização e análise dos exames.
6. **Unidade de Saúde**: Local onde o paciente recebe atendimento médico e solicita exames.
7. **Análise Clínica**: Exames laboratoriais de sangue, urina e fezes.
8. **Análise Citopatológica**: Exames de células coletadas por raspagem, como o Papanicolau.
9. **Análise Histopatológica**: Exames de tecidos coletados por biópsia.
10. **SLA (Acordo de Nível de Serviço)**: Parâmetros que definem os níveis de serviço esperados, como tempo de resposta e qualidade.

## 3. Modelo UML

O Modelo UML representa as classes identificadas no domínio, destacando as entidades, objetos de valor, agregados e eventos de domínio. Este modelo ajuda a visualizar a estrutura do sistema e as relações entre os diferentes componentes.

![Modelo UML](uml-model.png)

## 4. Diagrama dos Contextos Delimitados

O Diagrama dos Contextos Delimitados enfatiza as integrações entre os diferentes contextos do sistema. Ele destaca os modelos de Parceria, Fornecedor, Shared Kernel, Conformista e Camada Anticorrupção.

![Diagrama dos Contextos Delimitados](bounded-contexts.png)

## 5. Fluxo Upstream e Downstream

O diagrama de Fluxo Upstream e Downstream evidencia quando o fluxo de informações é ascendente (upstream) ou descendente (downstream) entre os diferentes contextos do sistema.

![Fluxo Upstream e Downstream](upstream-downstream.png)
