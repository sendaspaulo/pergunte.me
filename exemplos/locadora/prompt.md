# Painel de frota da locadora Curva

## Objetivo
Construa um site em português do Brasil para a atendente da Curva.
Durante uma ligação, ela precisa consultar a disponibilidade e a
diária de um carro. Depois, deve conseguir atualizar a frota.

## Dados e regras
- Dê a cada veículo um ID estável. Cadastre marca e modelo, placa,
  categoria, diária em reais e situação.
- Categorias: Econômico, Sedã, SUV e Utilitário.
- Situações: Disponível, Locado e Manutenção. A atualização é manual.
- Exija modelo e placa. Aceite ABC1234 e ABC1D23. Remova hífens e
  converta a placa para maiúsculas antes de verificar duplicidade.
  Na edição, ignore o próprio veículo nessa comparação.
- Aceite apenas diárias positivas com até duas casas decimais.

## Tela e operações
- Mostre o total da frota e os totais por situação, mesmo com filtros.
- Liste modelo, categoria, placa, diária, situação e ações.
- Permita cadastrar, consultar, editar e excluir veículos.
- Combine busca por trecho do modelo ou da placa com o filtro de
  situação. Exiba uma mensagem quando a busca não retornar veículos.
- Ao excluir, mostre modelo e placa. Permita cancelar ou confirmar.

## Implementação
- Use HTML, CSS e JavaScript e entregue os arquivos do site estático.
- Inicie com seis carros fictícios. Salve alterações no navegador.
- Limite esta versão à gestão da frota.

## Critérios de aceite
- Cadastre um carro e tente repetir a placa com hífen e minúsculas.
- Localize o carro combinando a busca e o filtro de situação.
- Edite a diária e a situação e confira os valores após recarregar.
- Cancele uma exclusão e verifique se o carro continua na lista.
  Depois, confirme a exclusão e confira a remoção e os totais.
- Execute os testes e relate os resultados observados.
