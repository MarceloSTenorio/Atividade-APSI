# Contexto
### O projeto consiste em desenvolver uma aplicação, bem como sua documentação, para uma clínica veterinária chamada PetClinic. A elicitação dos requisitos foi feito a partir de uma entrevista, que está transcrita a seguir.


## 1. Entrevista

*Entrevistadora: Grace Murray Hopper*
*Entrevistada: Barbara Liskov*

### Pergunta 1:
O que você precisa em seu sistema?
> R: O sistema deverá ter uma área exclusiva para lançar, deletar e
alterar dados da agenda. Gerenciamento de pessoas onde o dono da
empresa poderá cadastrar, alterar ou deletar um novo funcionário ou um
novo cliente. Poderá ter um arquivo morto, onde posso deixar o histórico
das consultas e histórico de todo os animais atendidos pela empresa, pois
nesta sessão os arquivos só poderão ser consultados.

### Pergunta 2:
O seu sistema vai ter alguma restrição?
> R: Sim, somente pessoas devidamente cadastradas poderão ter
acesso aos dados do sistema.

### Pergunta 3:
Qual o valor que você está disposto a investir?
> R: A nossa empresa precisa gerenciar com mais precisão o estoque,
as compras, consultas e nossa agenda, por isso pensamos em investir no
máximo R$ 1.000,00 para o desenvolvimento total do projeto.

### Pergunta 4:
Você tem alguma coisa a acrescentar que não foi citada nesta
entrevista?
> R: De acordo com análise de sistemas em demonstração, vejo que
estes possuem uma velocidade de processamento um tanto quanto alta, por
este motivo gostaria que meu sistema tivesse essa agilidade.


## 2. Levantamento de Requisitos
### Após a entrevista, os seguintes requisitos foram identificados:

### 2.1 Requisitos Funcionais

- RF1. O sistema deve ter uma tela para logar no mesmo.
- RF2. O sistema deve ter uma tela para lançamento de um determinado
evento na agenda.
- RF3. O sistema deve ter a opção de alterar um determinado lançamento da
agenda.
- RF4. O sistema deve ter a opção de deletar um determinado lançamento da
agenda.
- RF5. O sistema deve ter uma opção para cadastrar uma nova pessoa
(cliente ou funcionário).
- RF6. O sistema deve ter a opção de alterar a pessoa cadastrada.
- RF7. O sistema deve ter a opção de deletar a pessoa anteriormente
cadastrada.
- RF8. O sistema deve possuir uma opção para cadastrar um novo
atendimento ou procedimento clínico.
- RF9. O sistema deve ter uma opção para alterar o histórico anteriormente
cadastrado.
- RF10. O sistema deve ter uma opção para mover o histórico anteriormente
cadastrado para o ‘arquivo morto’.
- RF11. O sistema deve ter uma opção para se conectar com o sistema
financeiro a fim de gerar a folha de pagamento (salários e demais gastos).


### 2.2 Requisitos Não-Funcionais

- RNF1. Confiabilidade – o sistema possui um sistema de backup automático
a fim de minimizar os riscos de uma possível falha.
- RNF2. Desempenho – todos os lançamentos não podem ultrapassar o
tempo limite de 7 segundos para serem inseridos no banco de dados.
- RNF3. Portabilidade – o sistema será desenvolvido para a plataforma
Windows tanto para a versão 32 e 64 bits. As migrações para outras
plataformas como IOS e Linux terão que passar um processo separado,
caso haja necessidade.
- RNF4. Segurança – todas as áreas do site tirando a tela inicial só poderão
ser acessadas mediante login e senha válida.


## 3. Atividades

1. Identifique os atores que poderão interagir com a aplicação
2. Identifique os sub-sistemas que serão desenvolvidos para compor a solução
3. Documente os requisitos usando histórias de usuários
4. Para cada história de usuário, descreva o mínimos de 3 critérios de aceitação usando BDD
5. Documente os seguintes Casos de Uso:
   - Cadastrar Medicamentos
   - Realizar cadastro de Funcionários
   - Gerenciar folha de pagamento
6. Identifique as classes, atributos e métodos desses cenários e coloque em uma tabela.
7. Desenha o diagrama de classes UML. Leve em consideração os relacionamentos vistos em sala.
