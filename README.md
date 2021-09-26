# Exe_Logica_Programa-o
Exercícios de Logica de Programação
amespace Logica_Programaçao2
{
    class Program
    {
        static void Main(string[] args)
        {

            Aula1();
        }

        static void Aula1()
        {
            // entrada de dados
            int tamanho = 10;
            int[] numeros = new int[tamanho];

            for (int i = 0; i < tamanho; i++)
            {
                Console.WriteLine("Digite um numero: ");
                numeros[i] = int.Parse(Console.ReadLine());
            }

            Console.WriteLine("---------- resumo da lista digitada --------------");
            for (int i = 0; i < tamanho; i++)
            {

                Console.WriteLine("Valor: " + numeros[i] + ", Posição: " + i);
            }

            // procurando o numero dentro do array
            Console.WriteLine("Digite um numero que deseja procurar: ");

            // variavel par achar o numero
            var ValorDig = Console.ReadLine();

            Console.WriteLine($"O numero digitado foi, {ValorDig}.");

            if (Array.Exists(numeros, x => x == Convert.ToInt32(ValorDig)))
            {

                Console.WriteLine("O numero foi encontrado: " + ValorDig);

                #region( par ou impar )

                if (Convert.ToInt32(ValorDig) % 2 == 0)
                    Console.WriteLine("O valor digitado é par.");

                else
                    Console.WriteLine("O valor digitado é impar.");

                #endregion

                Console.ReadKey();
            }
            else
            {
                Console.WriteLine("numero não encontrado.");
                Console.WriteLine("Refazer operação.");
                Console.ReadKey();

                Aula1();
            }
        }

    }
}
