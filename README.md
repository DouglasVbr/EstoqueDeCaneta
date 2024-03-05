# Produto

PARTE.1


// Arquivo: Produto.java
package estoque;

public class Produto {
    private String nome;
    private double preco;
    private int quantidade;
    
    // Construtor
    public Produto(String nome, double preco) {
        this.nome = "Caneta";
        this.preco = 2.50;
        this.quantidade = 0;
    }
    
    // Métodos acessores
    public String getNome() {
        return nome;
    }
    
    public double getPreco() {
        return preco;
    }
    
    public int getQuantidade() {
        return quantidade;
    }
    
    // Método para aumentar a quantidade do produto
    public void aumentarQuantidade(int quantidade) {
        this.quantidade += quantidade;
    }
    
    // Método para diminuir a quantidade do produto
    public void diminuirQuantidade(int quantidade) {
        if (this.quantidade >= quantidade) {
            this.quantidade -= quantidade;
        } else {
            System.out.println("Quantidade insuficiente em estoque.");
        }
    }
}



PARTE.2


// Arquivo: Main.java
package estoque;

public class Main {
    public static void main(String[] args) {
        // Criando um objeto Produto
        Produto produto1 = new Produto("Caneta", 2.50);
        
        // Exibindo informações do produto
        System.out.println("Nome: " + produto1.getNome());
        System.out.println("Preço: " + produto1.getPreco());
        System.out.println("Quantidade: " + produto1.getQuantidade());
        
        // Aumentando a quantidade do produto em estoque
        produto1.aumentarQuantidade(50);
        System.out.println("Nova quantidade: " + produto1.getQuantidade());
        
        // Diminuindo a quantidade do produto em estoque
        produto1.diminuirQuantidade(20);
        System.out.println("Quantidade após venda: " + produto1.getQuantidade());
    }
}
