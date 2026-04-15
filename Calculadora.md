using System;


class Program
{
    static void Main()
    {
    Console.WriteLine("Digite a area do imovel desejado");
double area = Convert.ToDouble(Console.ReadLine());

 Console.WriteLine("Digite o valor do metro quadrado:");
double metro_quadrado = Convert.ToDouble(Console.ReadLine());

double valor_m2 = 5000;
double valor_base = area * valor_m2;

Console.Write("Tipo (casa/apartamento): ");
string tipo = Console.ReadLine();

if (tipo == "apartamento")
{
    Console.Write("Qual andar? ");
    int andar = Convert.ToInt32(Console.ReadLine());

    double fator = 1 + (andar * 0.02);
    valor_base = valor_base * fator;
}
Console.Write("Quantos quartos? ");
int quartos = Convert.ToInt32(Console.ReadLine());

valor_base = valor_base + (quartos * 10000);

double aluguel = valor_base * 0.005;

Console.WriteLine("Valor final do imóvel: " + valor_base);
Console.WriteLine("Valor do aluguel: " + aluguel);
    }
}
