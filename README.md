# Melhor Combustível

### Código fonte:

``` using System;
using System.Globalization;

class Program {
  public static void Main (string[] args) {

CultureInfo CI = CultureInfo.InvariantCulture;
    
double alcool, gasolina, divisao;
string opcao = "S";

    while (opcao.Equals("S") || opcao.Equals("s")) {
      
      Console.Write("Digite o valor do Alcool: ");
      alcool = double.Parse(Console.ReadLine(), CI);

      Console.Write("Digite o valor da Gasolina: ");
      gasolina = double.Parse(Console.ReadLine(), CI);

      divisao = alcool / gasolina;
      if (divisao > 0.7) {
        Console.WriteLine("Abastecer com GASOLINA.");
      }
        else if (divisao < 0.7) {
          Console.WriteLine("Abastecer com ALCOOL.");
        }
        else {
          Console.WriteLine("Tanto faz.");
        }
        Console.Write("Deseja efetuar um novo cálculo (S/N)? ");
        opcao = Console.ReadLine();
    }
        Console.Write("FIM DO PROGRAMA!");
  }
}
