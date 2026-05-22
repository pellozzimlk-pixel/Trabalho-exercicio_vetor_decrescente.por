# Trabalho-exercicio_vetor_decrescente.por
programa
{
	funcao inicio()
	{
		// Inicializa o vetor com os 10 números não ordenados do exemplo
		inteiro vetor[10] = {2, 5, 1, 3, 4, 9, 7, 8, 10, 6}
		inteiro copia, i, j

		// Algoritmo de Ordenação Decrescente (Bubble Sort)
		// O primeiro laço controla quantas vezes vamos passar pelo vetor
		para (i = 0; i < 10; i++)
		{
			// O segundo laço compara os elementos vizinhos
			para (j = 0; j < 9; j++)
			{
				// Se o elemento atual for MENOR que o próximo, eles trocam de lugar
				// Isso garante que os maiores números "flutuem" para o início
				se (vetor[j] < vetor[j + 1])
				{
					copia = vetor[j]
					vetor[j] = vetor[j + 1]
					vetor[j + 1] = copia
				}
			}
		}

		// Saída de dados: Exibe o vetor já ordenado no console
		escreva("Vetor ordenado em ordem decrescente:\n")
		para (i = 0; i < 10; i++)
		{
			escreva(vetor[i], " ")
		}
		escreva("\n")
	}
}



programa
{
	funcao inicio()
	{
		// Declaração do vetor de 10 posições e das variáveis de controle
		inteiro vetor[10]
		inteiro i
		inteiro soma = 0
		real media

		// 1. Entrada de dados: Lê os 10 números inteiros fornecidos pelo usuário
		para (i = 0; i < 10; i++)
		{
			escreva("Digite o ", i + 1, "º número: ")
			leia(vetor[i])
			
			// Já vai acumulando a soma total dos elementos durante a leitura
			soma = soma + vetor[i]
		}

		escreva("\n-----------------------------------------\n")
		escreva("                 SAÍDA                   ")
		escreva("\n-----------------------------------------\n")

		// 2. Elementos nos índices ímpares (índices 1, 3, 5, 7, 9)
		escreva("Elementos nos índices ímpares:\n")
		para (i = 0; i < 10; i++)
		{
			// Verifica se o ÍNDICE (a posição i) é ímpar
			se (i % 2 != 0)
			{
				escreva(vetor[i], " ")
			}
		}
		escreva("\n\n")

		// 3. Elementos pares (os números armazenados que são divisíveis por 2)
		escreva("Elementos pares:\n")
		para (i = 0; i < 10; i++)
		{
			// Verifica se o VALOR dentro do vetor é par
			se (vetor[i] % 2 == 0)
			{
				escreva(vetor[i], " ")
			}
		}
		escreva("\n\n")

		// 4. Exibe a Soma
		escreva("Soma:\n", soma, "\n\n")

		// 5. Cálculo e exibição da Média (armazenada em variável do tipo real)
		// Como o enunciado avisa que o Portugol arredonda operações com inteiros,
		// fazemos a divisão direta usando o total de elementos (10)
		media = soma / 10
		escreva("Média:\n", media, "\n")
	}
}
