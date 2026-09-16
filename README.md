# POO, TRABALHANDO EXERCÍCIOS EM PYTHON.

## Exercícios
  1. Classe e Objeto Crie uma classe Pessoa com os atributos nome e idade. Crie um objeto e exiba seus atributos.

  2. Construtor Crie uma classe Produto com os atributos nome, preco e estoque, inicializados por um construtor. Crie dois produtos diferentes e exiba seus dados.

  3. Métodos Crie uma classe Aluno com os atributos nome e nota. Implemente o método aprovado(), que deve retornar true quando a nota for maior ou igual a 6.

  4. this / self Crie uma classe Retangulo com os atributos largura e altura. Utilize this (ou self) para inicializá-los no construtor e implemente um método calcularPerimetro().

  5. Modificadores de acesso Crie uma classe ContaBancaria com o atributo saldo como privado. Implemente os métodos depositar(valor) e consultarSaldo(), sem permitir que o saldo seja alterado diretamente.

## PRIMEIRO EXERCÍCIO.

```python
class Pessoa:

    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

pessoa = Pessoa("Maria", 16)
print(pessoa.nome)
```

# SEGUNDO EXERCÍCIO.

```python
class Produto1:

    def __init__(self, nome, preco, estoque):
        self.nome = nome
        self.preco = preco
        self.estoque = estoque
      
class Produto2:

    def __init__(self, nome, preco, estoque):
        self.nome = nome
        self.preco = preco
        self.estoque = estoque
      
Produto1 = Produto1("Chocolate", 5.00, 12)
print(f"Nome produto: {Produto1.nome} ")
print(f"Preço: {Produto1.preco}")
print(f"Estoque: {Produto1.estoque}")

Produto2 = Produto2("Bolacha Salgada", 3.50, 10)
print(f"Nome produto: {Produto2.nome} ")
print(f"Preço: {Produto2.preco}")
print(f"Estoque: {Produto2.estoque}")
```

# TERCEIRO EXERCÍCIO.

```python
class Aluno:

    def __init__(self, nome, nota):
      self.nome = nome  
      self.nota = nota

Aluno1 = Aluno("José da Silva", 5)
print(f"Nome:  {Aluno1.nome}")
print(f"Nota:  {Aluno1.nota}")

nota = Aluno1.nota

if nota >= 6:
    print("aprovado")

else:
 print("reprovado")
```

# QUARTO EXERCÍCIO.

```
class retangulo:

  def __init__(self, largura, altura):
        self.largura = largura
        self.altura = altura

  def calcular_perimetro(self, largura, altura):
        return  2 * (self.largura + self.altura)

retangulo = retangulo(5,10)
perimetro = retangulo.calcular_perimetro(2, 5)

print(f"largura: {retangulo.largura}")
print(f"altura: {retangulo.altura}")
print(f"perimetro: {perimetro}")
```

# QUINTO EXERCÍCIO.

```python
class conta_bancaria:
  def __init__(self, saldo):
    self.__saldo = saldo

  def depositar(self, valor):
    if valor > 0:
      self.__saldo += valor
      print(f"Depositado {valor} com sucesso.")
    else:
      print("Valor inválido")

  def consultar(self):
    return self.__saldo

conta = conta_bancaria(0)
deposito = float(input("Valor a depositar: "))
conta.depositar(deposito)

print(f"Valor da conta: {conta.consultar()}")
```
