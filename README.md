Esquema Conceitual - Sistema de Oficina Mecânica
🛠️ Descrição do Projeto
Este repositório contém o esquema conceitual desenvolvido para o sistema de controle e gerenciamento de ordens de serviço de uma oficina mecânica. O objetivo deste projeto é organizar as informações sobre os clientes, veículos, equipes de mecânicos e ordens de serviço de forma clara e eficiente, permitindo o controle das atividades realizadas na oficina.

📖 Contexto
O esquema conceitual foi criado com base na seguinte narrativa fornecida:

Clientes levam seus veículos à oficina para manutenção ou revisões periódicas.
Veículos são designados a equipes de mecânicos, que identificam os serviços necessários e preenchem uma Ordem de Serviço (OS).
Cada OS inclui detalhes como data de emissão, data de entrega, valor dos serviços e status.
O custo da OS é composto pelo valor da mão-de-obra e das peças utilizadas, com base em uma tabela de referência.
Mecânicos possuem informações como código, nome, endereço e especialidade.
A equipe de mecânicos avalia e executa os serviços autorizados pelo cliente.
🎯 Objetivo
Modelar o esquema conceitual para representar o funcionamento do sistema da oficina, abrangendo:

Entidades principais (clientes, veículos, mecânicos, ordens de serviço, serviços e peças).
Relacionamentos entre as entidades.
Atributos relevantes para cada entidade e relacionamento.
🧩 Estrutura do Esquema Conceitual
Entidades
Clientes

Código do Cliente (PK)
Nome
Telefone
Endereço
Veículos

Placa (PK)
Modelo
Marca
Ano
Código do Cliente (FK)
Mecânicos

Código do Mecânico (PK)
Nome
Endereço
Especialidade
Ordens de Serviço (OS)

Número da OS (PK)
Data de Emissão
Data de Conclusão
Valor Total
Status
Serviços

Código do Serviço (PK)
Descrição
Valor da Mão de Obra
Peças

Código da Peça (PK)
Descrição
Valor
Relacionamentos
Clientes - Veículos

Um cliente pode possuir vários veículos.
Cada veículo pertence a um único cliente.
Veículos - Ordens de Serviço

Um veículo pode estar associado a várias ordens de serviço.
Cada OS está vinculada a um único veículo.
Mecânicos - Ordens de Serviço

Uma equipe de mecânicos é atribuída a cada OS.
Um mecânico pode participar de várias OS.
Ordens de Serviço - Serviços/Peças

Uma OS pode incluir múltiplos serviços e peças.
Cada serviço e peça pode estar associado a várias OS.
🚀 Como Utilizar
Clone este repositório:
bash
Copiar código
git clone https://github.com/seu-usuario/sistema-oficina-mecanica.git
Abra o arquivo do esquema conceitual (esquema_conceitual.png) para visualizar o modelo.
📝 Notas e Decisões de Design
Tabela de Referência: Foi assumido que a tabela de referência de mão de obra está embutida nos valores de "Serviços".
Equipes de Mecânicos: Cada OS é atribuída a uma equipe, representada por um grupo de mecânicos, mas não detalha a composição da equipe.
Faltas de Informação: Onde a narrativa não especificou informações adicionais, foi assumido o contexto padrão do domínio da oficina mecânica.

![MecanicaOS](https://github.com/user-attachments/assets/d0ed6cec-034c-4828-859c-9306490a45d8)

