# Otimizacao_do_Sistema_Bancario_com_Funcoes_Python
Desafio da Formação Python Developer pela DIO - Sistema bancário, considerando que não está atribuída questões como: segurança, autenticação de usuário, registro de transações, entre outros, tendo em vista que o Sistema Bancário poderia conter frameworks como o Django ou Flask para criar aplicativos bancários mais robustos e seguros.

Abaixo segue o código da Otimização do Sistema Bancário da Formação em Python Developer ministrado pela Instituição Digital Innovatio One:

# Definindo uma classe para representar uma conta bancária
class ContaBancaria:
    def __init__(self, nome, saldo=0):
        self.nome = nome
        self.saldo = saldo

    def deposito(self, valor):
        if valor > 0:
            self.saldo += valor
            print(f'Depósito de R${valor} realizado com sucesso. Novo saldo: R${self.saldo}')
        else:
            print('Valor de depósito inválido.')

    def saque(self, valor):
        if valor > 0 and valor <= self.saldo:
            self.saldo -= valor
            print(f'Saque de R${valor} realizado com sucesso. Novo saldo: R${self.saldo}')
        else:
            print('Valor de saque inválido ou saldo insuficiente.')

    def extrato(self):
        print(f'Nome do titular: {self.nome}')
        print(f'Saldo atual: R${self.saldo}')


# Exemplo de uso
if __name__ == "__main__":
    conta = ContaBancaria("João")
    
    conta.deposito(1000)
    conta.saque(500)
    conta.extrato()
