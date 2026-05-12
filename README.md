# avaliacao_01_algoritmos
Gabrielly Costa Dos Santos
Técnico De Informatica para internet
Sistema de gerenciamento de funcionarios usando matrizes

algoritmo "funcionarios"

var
  funcionarios: vetor [1..10,1..4] de caractere
  opcao, i,totalcadastrados: inteiro
  nome:caractere
  encontrado:logico

inicio
  totalcadastrados <- 0
  opcao <- 0

  enquanto opcao <> 4 faca
    escreval("---menu do sistema---")
    escreval("1 - cadastrar um funcionario")
    escreval("2 - pesquisar um funcionario pelo nome")
    escreval("3 - exibir todos os funcionarios")
    escreval("4 - sair do programa")
    escreval("escolha uma opcao:")
    leia(opcao)

    escolha opcao
      opcao 1
      se totalcadastrados < 10 entao
        totalcadastrados <-
        totalcadastrados + 1
        escreval ("cadastro do", totalcadastrados,"funcionario")
        escreva ("nome:")
        leia(funcionarios[totalcadastrados, 1])
        escreva ("cargo:")
        leia(funcionarios[totalcadastrados, 2])
        escreva("salario:")
        leia(funcionarios[totalcadastrados, 3])
        escreva("data de admissao:")
        leia(funcionarios[totalcadastrados, 4])
        escreval("funcionario cadastrado com sucesso")
      senao
        escreval("erro: limite maximo de 10 funcionarios atingido")
      fimse

      opcao 2
      escreva("digite o nome do funcionario")
      leia(nome)
      encontrado <- falso
      para i de 1 ate
      totalcadastrados
      faca
      se funcionarios[i, 1]= nome entao
        escreval("funcionamento encontrado:")
        escreval("nome:", funcionarios[i, 1])
        escreval("cargo:",funcionarios[i, 2])
        encontrado <- verdadeiro interrompa
      fimse
    fimpara
    se nao encontrado entao
      escreval("nenhum resultado para a pesquisa")
    fimse

    opcao 3
    se totalcadastrados = 0 entao
      escreval("nao existem funcionarios cadastrados")
    senao
      escreval("lista de funcionarios")
      escreval("----------------------------------------------------------")
      escreval("nome    |     cargo      |      salario    |      admissao")
      escreval("----------------------------------------------------------")
      para i de 1 ate
      totalcadastrados faca
      escreval(funcionarios[i, 1]:10, " | ", funcionarios[i, 2]:10," | ", funcionarios[i, 3]:10," | ", funcionarios[i, 4])
    fimse

    opcao 4
    escreval("encerramento o programa")
  outrocaso
    escreval("opcao invalida! tente novamente")
fimescolha
escreval("")
fimenquanto



fimalgoritmo
