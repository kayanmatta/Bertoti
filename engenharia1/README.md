1.  Embora seja menos tangivel as criações dos engenheiros de sofware comparado ao trabalho dos outros engenheiros, ainda sim precisa de conhecimento teórico e constroem algo real, mesmo as teórias sendo menos rigorosas, quanto mais a tecnologia for inserida em nossas vidas mais vamos ter que adotar e confiar em metodos da engenharia de software.


2.A engenhria de software necessita de planejamento, nâo só programaçâo, necessita se adptar e tentar prever as possiveis mudanças com o tempo, se ele ira crescer ou se tera que deixar de usar alguma linguagem para que seja melhor o desempenho.

3.a) O uso de uma linguagem mais dificil para melhor desempenho de sem código ou aplicativo.
b)desempenho e escalabilidade, o desempenho focando no tempo de resposta e na eficiencia do sistema, pórem, a escabilidade envolve em produzir sistemas que aguentem grandes cargas de trabalho, de usuários e volume de dados maiores.
c)A velocidade custuma ser crucial para cumprir os prazos dos projetos e grandes demandas,porém, manter a qualidade do código tambem é sim importante para garantir um software mais sustentavel.

4.A mensagem principal da imagem é sempre começe por uma versão simples porém funcional, ao invés de construir partes que só irão funcionar ao final. Isso permite aprender desde o início do projeto.

5.
```
public class Livro {
    private String titulo;
    private String autor;

    public Livro(String titulo, String autor) {
        this.titulo = titulo;
        this.autor = autor;
    }

    public String getTitulo() {
        return titulo;
    }

    public String getAutor() {
        return autor;
    }

    public String toString() {
        return "Livro: " + titulo + " | Autor: " + autor;
    }
}

import java.util.ArrayList;

public class Biblioteca {
    private ArrayList<Livro> livrosDisponiveis;

    public Biblioteca() {
        livrosDisponiveis = new ArrayList<>();
    }

    public void adicionarLivro(Livro livro) {
        livrosDisponiveis.add(livro);
        System.out.println("Livro adicionado: " + livro);
    }
    public void removerLivro(String titulo) {
        for (Livro livro : livrosDisponiveis) {
            if (livro.getTitulo().equalsIgnoreCase(titulo)) {
                livrosDisponiveis.remove(livro);
                System.out.println("Livro removido: " + livro);
                return;
            }
        }
        System.out.println("Livro não encontrado: " + titulo);
    }

    public void listarLivros() {
        System.out.println("Livros na biblioteca:");
        for (Livro livro : livrosDisponiveis) {
            System.out.println(livro);
        }
    }
}
public class TesteBiblioteca {
    public static void main(String[] args) {
        Biblioteca biblioteca = new Biblioteca();

        Livro livro1 = new Livro("Dom Casmurro", "Machado de Assis");
        Livro livro2 = new Livro("A Revolução dos Bichos", "George Orwell");
        Livro livro3 = new Livro("1984", "George Orwell");

        biblioteca.adicionarLivro(livro1);
        biblioteca.adicionarLivro(livro2);
        biblioteca.adicionarLivro(livro3);

        biblioteca.listarLivros();

        biblioteca.removerLivro("1984");

        biblioteca.listarLivros();
    }
}
```
