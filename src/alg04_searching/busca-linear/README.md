# Algoritmo de Busca Linear

A busca linear é um algoritmo de busca fundamental que itera por uma lista de elementos um por um, comparando cada
elemento ao valor alvo. Se o valor alvo for encontrado, a busca para e retorna o índice do elemento. Caso contrário, a
busca continua até que o fim da lista seja alcançado, momento em que retorna -1 para indicar que o valor alvo não foi
encontrado. Busca linear também é conhecida como **busca sequencial** .

## Exemplo Visual

![Linear-search-algorithm-1.webp](..%2F..%2F..%2F..%2F..%2FAppData%2FLocal%2FTemp%2FLinear-search-algorithm-1.webp)
![Linear-search-algorithm-2.webp](..%2F..%2F..%2F..%2F..%2FAppData%2FLocal%2FTemp%2FLinear-search-algorithm-2.webp)
![Linear-search-algorithm-3.webp](..%2F..%2F..%2F..%2F..%2FAppData%2FLocal%2FTemp%2FLinear-search-algorithm-3.webp)

Abaixo está a implementação do algoritmo de busca linear utilizando a linguagem Java com base nesse exemplo mostrado
acima:

## Exemplo em Java
``` Java

public class BuscaLinear {
    public static int buscaLinear(int[] arr, int key) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == key) {
                return i; // Retorna o índice onde a chave foi encontrada
            }
        }
        return -1; // Retorna -1 se a chave não for encontrada
    }

    public static void main(String[] args) {
        int[] arr = {10, 50, 30, 70, 80, 20, 90, 40}; // Lista de Números
        int key = 30; // Valor a ser procurado
        
        int resultado = buscaLinear(arr, key);
        
        if (resultado != -1) {
            System.out.println("Elemento encontrado no índice: " + resultado);
        } else {
            System.out.println("Elemento não encontrado.");
        }
        
        // Output: Elemento encontrado no índice: 2
    }
}

```

## Em quais cenários devo utilizar o Algoritmo de Busca Linear?
1. **Pequenos conjuntos de dados:** Quando o conjunto de dados é relativamente pequeno (por exemplo, menos de algumas
   centenas de elementos), a busca linear pode ser eficiente porque o número de comparações necessárias é pequeno.

2. **Dados não classificados:** Ele é particularmente útil para dados não classificados, pois não requer
   nenhuma classificação prévia dos elementos.

3. **Implementação simples:** A busca linear é um dos algoritmos de busca mais simples de implementar, o que a torna
   adequada para iniciantes e fins educacionais.

4. **Natureza iterativa:** Por se tratar de um algoritmo iterativo, isso o torna fácil de entender e depurar.

5. **Aplicações em tempo real:** Em certas aplicações em tempo real, onde o conjunto de dados muda constantemente, a
   pesquisa linear pode ser mais eficiente do que outros algoritmos de busca que exigem pré-processamento ou
   classificação.

6. **Memória limitada:** A busca linear requer sobrecarga mínima de memória, pois ela só precisa armazenar o elemento
   atual que está sendo comparado. Isso a torna adequada para sistemas com recursos de memória limitados.

## Quais são as suas vantagens?
- **Simplicidade:** A busca linear é um dos algoritmos de busca mais simples de entender e implementar.

- **Eficiência para pequenos conjuntos de dados:** para pequenos conjuntos de dados, a pesquisa linear pode ser mais
  eficiente
  do que outros algoritmos de pesquisa que exigem pré-processamento ou classificação.

- **Dados não classificados:** a pesquisa linear pode ser usada para pesquisar dados não classificados sem qualquer
  classificação prévia.

- **Aplicações em tempo real:** a pesquisa linear pode ser útil em aplicações em tempo real, onde o conjunto de dados
  muda
  constantemente.

- **Sobrecarga de memória limitada:** a pesquisa linear requer sobrecarga de memória mínima, o que a torna adequada para
  sistemas com recursos de memória limitados.

## Quais são as suas desvantagens?
- **Ineficiência para grandes conjuntos de dados:** para grandes conjuntos de dados, a pesquisa linear pode ser
  ineficiente
  porque exige iteração por toda a lista para cada pesquisa.

- **Não adequado para dados classificados:** a pesquisa linear não é tão eficiente quanto outros algoritmos de
  pesquisa (por
  exemplo, pesquisa binária) para dados classificados.

## Complexidade de Tempo:
A complexidade de tempo nos diz o quanto o algoritmo demora para executar em relação ao tamanho da entrada (neste caso,
o número de elementos na lista).

### Análise:
1. No pior caso, o algoritmo vai ter que percorrer todos os elementos da lista. Ou seja, se a lista tem `n` elementos, o
algoritmo verifica todos eles até encontrar a chave ou concluir que ela não existe.

2. Se o elemento que estamos procurando está no último índice da lista ou não está presente, o algoritmo precisa passar por
todos os elementos.

Então, a complexidade de tempo é O(n), onde `n` é o número de elementos na lista.

### Explicando através de Analogia:
Imagine que você está procurando uma chave em uma gaveta com vários compartimentos. Se a chave estiver no último
compartimento, você terá que abrir todos os compartimentos um por um. Isso é o que acontece na busca linear: no pior
caso, você verifica cada item até encontrar o que quer.

## Complexidade de Espaço:
A complexidade de espaço nos diz quanto de memória o algoritmo precisa para funcionar. A busca linear não usa estruturas
de dados adicionais (como listas ou mapas), ela apenas percorre o array dado. Ela usa uma quantidade constante de
memória para armazenar algumas variáveis, como o índice i e o valor retornado, mas nada além disso.

Portanto, a complexidade de espaço é O(1), o que significa que ela precisa de uma quantidade constante de memória,
independentemente do tamanho da lista.

### Explicando através de Analogia:
Pensando na gaveta novamente: mesmo que a gaveta tenha muitos compartimentos, você só precisa de um espaço para
verificar se a chave está em cada compartimento, sem precisar de mais espaço.

## Conclusão
A busca linear é um algoritmo de busca simples e eficiente que é particularmente útil para pequenos conjuntos de dados,
dados não classificados e aplicações em tempo real. Embora não seja tão eficiente quanto outros algoritmos de busca para
grandes conjuntos de dados classificados, sua simplicidade e facilidade de implementação o tornam uma ferramenta valiosa
em vários cenários.