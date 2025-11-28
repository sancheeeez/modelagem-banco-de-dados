README – Sistema de Banco de Dados para Delivery / Restaurante
🍔 Sobre o Projeto

Este projeto implementa a modelagem de um banco de dados para um sistema de delivery, incluindo clientes, funcionários, motoboys, pedidos e itens do menu.
O modelo foi construído com base em um Diagrama Entidade-Relacionamento (ER), garantindo organização, integridade e clareza nos relacionamentos.

O sistema permite registrar:

clientes e seus pedidos,

funcionários que efetuam pedidos,

motoboys responsáveis pela entrega,

itens do menu,

valores, pagamentos e itens consumidos.

🧱 Modelagem do Banco de Dados

O banco é composto por 5 entidades principais:

clientes

funcionario

motoboy

menu

pedido

Cada entidade possui seus próprios atributos e se relaciona de maneira estruturada com as demais.

🧩 Entidades e Atributos
👤 1. clientes

Atributos:

cpf (PK)

nome

pagamento

pedido

Função: armazena os dados dos clientes que fazem pedidos no sistema.

🧑‍💼 2. funcionario

Atributos:

cpf (PK)

nome

qualificacoes

Função: registra dados dos funcionários que efetuam os pedidos.

Relacionamento:

Um funcionário efetua de 1 a N pedidos.

🛵 3. motoboy

Atributos:

id_pedido (PK)

nome

valor

pagamento

pedido

Função: armazena motoboys que realizam entregas.

Relacionamento:

Um motoboy realiza de 1 a N entregas.

🍽️ 4. menu

Atributos:

id (PK)

nome

valor

item

bebida

sobremesa

lanche

Função: representa os itens disponíveis no cardápio.

Relacionamento:

O menu é associado aos pedidos pela relação “realiza”.

🧾 5. pedido

Atributos:

id (PK)

item

valor

Função: representa o pedido realizado pelo cliente.

Relacionamentos importantes:

Um cliente realiza de (1,1) pedidos.

Um pedido pode existir ou não estar associado ainda → (0,n).

Um funcionário efetua (1,n) pedidos.

Um motoboy realiza entregas de (1,n).

Um pedido inclui itens do menu de (1,n).

🔗 Relacionamentos do Sistema
🤝 Cliente — Pedido

(1,1) Cliente realiza (0,n) Pedido
Um cliente pode realizar vários pedidos; um pedido pertence a um único cliente.

🧑‍💼 Funcionário — Pedido

(1,n) Funcionário efetua (1,1) Pedido
Cada pedido é lançado por um funcionário do sistema.

🛵 Motoboy — Pedido

(1,n) Motoboy realiza (0,1) Pedido
Um motoboy pode fazer várias entregas; um pedido tem no máximo um motoboy responsável.

🍽️ Menu — Pedido

(1,n) Menu contém (1,n) Pedido
Um pedido pode ter vários itens do menu, e cada item pode aparecer em vários pedidos.
