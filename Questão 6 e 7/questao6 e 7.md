``` Mermaid
classDiagram
    %% 6. Identifique as classes, atributos e métodos desses cenários e coloque em uma tabela.
    %% 7. Desenha o diagrama de classes UML. Leve em consideração os relacionamentos vistos em sala.
    class Cliente {
        -String nome_cliente
        -Int    cod_cliente
        Animal.get_codAnimal() :int
        +get_nomeCliente() :String
        +get_codCliente()  :int
        +set_nomeCliente()
        +set_codCliente()
    }
    
    class Funcionario {
        -String nome_funcionario
        -String cpf
        -Int    horas_trabalhadas
        -Const  horas_esperadas
        -Int    cod_funcionario
        -Int    falta_horas
        +get_nomeFuncionario() :String
        +get_cpf() :String
        +get_codFuncionario() :String
        +set_nomeFuncionario()
        +set_cpf()
        +set_codFuncionario()
        +set_horasTrabalhadas(this.horas_trabalhadas + horas_trabalhadas)
        +carga_horária(cod_funcionario,horas_trabalhadas,horas_esperadas) :String nome_funcionario + Int falta_horas
    }
    
    class Animal {
        -String nome_animal
        -String cor_animal
        -Int    idade_animal
        -String sex_animal
        +Int    cod_animal
        +get_nomeAnimal()   :String
        +get_corAnimal()    :String
        +get_idadeAnimal()  :int
        +get_sexAnimal()    :String
        +get_codAnimal()    :int
        +set_nomeAnimal()
        +set_corAnimal()
        +set_idadeAnimal()
        +set_sexAnimal()
        +set_codAnimal()
    }
    
    class Medicacao {
        -Int    cod_medicacao
        -String nome_medicacao
        -Date   data_validade
        -Int    qnt_medicacao
        +get_codMedicacao()  :int
        +get_nomeMedicacao() :String
        +get_dataValidade()  :Date
        +get_qntMedicacao() :int
        +set_codMedicacao()
        +set_nomeMedicacao()
        +set_dataValidade()
        +set_qntMedicacao()
    }
    
    class Consulta {
        -Date data_consulta
        Funcionario.get_codFuncionario() :int
        Animal.get_codAnimal() :int
        Cliente.get_codCliente() :int
        Medicacao.get_codMedicacao() :int
        Medicacao.get_nomeMedicacao() :String
    }

Cliente "1"<.."1..*"        Animal   :Depende
Cliente "1"-->"1"           Consulta :Participa
Animal "1"-->"1..*"         Consulta :Possui
Funcionario "1..*"-->"*"    Consulta :Participa
Medicacao "1..*"-->"*"      Consulta :Utilizada

```