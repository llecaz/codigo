PRIMEIRO EXERCÍCIO PYTHON

class Pessoa:

    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade



pessoa = Pessoa("Maria", 16)
print(pessoa.nome)

SEGUNDO EXERCÍCIO






TERCEIRO EXERCÍCIO

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
  
