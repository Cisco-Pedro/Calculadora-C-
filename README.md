# Calculadora-C-
Esta é uma calculadora simples desenvolvida em C#, que permite realizar a operação de adição. O programa foi implementado utilizando a linguagem C# e a plataforma .NET. A calculadora é uma ótima ferramenta para aprendizado e prática de programação em C# e pode ser utilizada como base para a criação de projetos mais complexos.
using System;
namespace CalculadoraC
{
    class Calculadora
    {
        static void Main()
        {
            bool opcao = true;

            Console.WriteLine("Olá, irei realizar a soma de números que você desejar.");

            Console.WriteLine("Digite o valor inicial:");
            float.TryParse(Console.ReadLine(), out float inicial);

            while (opcao)
            {
                Console.WriteLine("Digite o número para soma:");
                float.TryParse(Console.ReadLine(), out float n1);
                inicial += n1;
                Console.WriteLine("A soma até o momento é {0}", inicial);
                Console.WriteLine("Deseja sair do programa? 1-Sim 2-Não");
                int.TryParse(Console.ReadLine(), out int saida);
                switch (saida)
                {
                    case 1:
                        Console.WriteLine("Saindo do programa.");
                        opcao = false;
                        break;
                    case 2:
                        Console.WriteLine("Continuar a soma.");
                        break;
                    default:
                        Console.WriteLine("Opção inválida. Reiniciando a soma.");
                        break;
                }
            }
        }
    }
}
