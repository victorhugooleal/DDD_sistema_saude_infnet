práti
# Domínio Tático do Projeto de Sistema de Saúde

## Entidades

1. **Paciente**
   - Atributos: id, nome, dataNascimento, CPF, endereco, contato
   - Descrição: Representa uma pessoa que recebe atendimento médico e realiza exames.

2. **Médico**
   - Atributos: id, nome, CRM, especialidade
   - Descrição: Profissional de saúde que solicita exames e realiza consultas.

3. **Unidade de Saúde**
   - Atributos: id, nome, tipo, endereco
   - Descrição: Local onde o paciente recebe atendimento médico e coleta de exames.

4. **Exame**
   - Atributos: id, tipo, subTipo, parametros, resultado
   - Descrição: Procedimento realizado para obter informações sobre a saúde do paciente.

5. **Solicitação de Exame**
   - Atributos: id, paciente, medico, unidadeSaude, exames, dataSolicitacao
   - Descrição: Pedido formal feito pelo médico para a realização de um exame.

6. **Prontuário**
   - Atributos: id, paciente, dataCriacao, historico
   - Descrição: Registro eletrônico que contém o histórico médico do paciente, incluindo exames e consultas.

7. **Laudo**
   - Atributos: id, exame, resultado, dataEmissao, assinaturaDigital
   - Descrição: Documento que contém o resultado do exame, assinado por um médico patologista.

8. **Faturamento**
   - Atributos: id, exame, custo, precoVenda, precoReembolso
   - Descrição: Processo de cobrança pelos serviços prestados, incluindo exames realizados.

## Objetos de Valor

1. **Endereço**
   - Atributos: rua, numero, cidade, estado, CEP
   - Descrição: Representa o endereço de uma entidade.

2. **Contato**
   - Atributos: telefone, email
   - Descrição: Representa as informações de contato de uma entidade.

3. **Parâmetro de Exame**
   - Atributos: nome, valor
   - Descrição: Critérios específicos medidos durante um exame, como colesterol ou glicemia.

## Agregados

1. **Paciente**
   - Entidades: Paciente, Prontuário
   - Descrição: O paciente é o agregado raiz que contém o prontuário e todas as informações relacionadas ao seu histórico médico.

2. **Solicitação de Exame**
   - Entidades: Solicitação de Exame, Exame
   - Descrição: A solicitação de exame é o agregado raiz que contém os exames solicitados pelo médico.

## Eventos de Domínio

1. **ExameSolicitado**
   - Descrição: Evento disparado quando um exame é solicitado pelo médico.
   - Atributos: idSolicitacao, idPaciente, idMedico, idUnidadeSaude, dataSolicitacao

2. **ExameRealizado**
   - Descrição: Evento disparado quando um exame é realizado.
   - Atributos: idExame, idSolicitacao, resultado, dataRealizacao

3. **LaudoEmitido**
   - Descrição: Evento disparado quando um laudo é emitido.
   - Atributos: idLaudo, idExame, resultado, dataEmissao, assinaturaDigital

4. **FaturamentoGerado**
   - Descrição: Evento disparado quando o faturamento é gerado.
   - Atributos: idFaturamento, idExame, custo, precoVenda, precoReembolso, dataFaturamento
