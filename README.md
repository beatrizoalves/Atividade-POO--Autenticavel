# Atividade-POO--Autenticavel
Estudo 

abstract class Autenticavel{
  bool autentica (int senha);
}

class Funcionario{
  String nome;

  Funcionario(this.nome);
}

class Gerente extends Funcionario implements Autenticavel{
  int _senha;

  Gerente (String nome, this._senha) : super(nome);

  @override
  bool autentica (int senha) {
    if (senha == _senha){
      return true;

    }else{
      return false;
    }    
  }
}

void main () {
  Gerente gerente = Gerente("Beatriz", (92523284));
  int senha = 9359888;
  
  bool ok = gerente.autentica(senha);
  print('Senha autenticada com sucesso!');



}


