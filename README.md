# Produto

PARTE.1

package produto;

public class Produto {

    public static void main(String[] args) {
        Produto2 Produto = new Produto2("Caneta", 2.50, 100);
        System.out.println("NOME:" + Produto.getNome());
        System.out.println("PREÇO:" + Produto.getPreco());
        System.out.println("QTD:" + Produto.getQtd());

        Produto.AumentarQtd(50);
        System.out.println("QTD APÓS O ALMENTO:" + Produto.getQtd());

        Produto.DiminuirQtd(30);
        System.out.println("QTD APÓS DIMINUIÇÃO:" + Produto.getQtd());
    }
    
}




PARTE.2
//Classe Produto:
//Crie uma classe Produto com os seguintes atributos: nome, preco, quantidade.
//Implemente um método construtor que inicialize os atributos nome e preco,
//e defina a quantidade como zero. Em seguida, crie métodos acessores para os atributos nome,
//preco e quantidade, e métodos para aumentar e diminuir a quantidade do produto.
package produto;

public class Produto2 {

    //variaveis
    private String Nome;
    private double preco;
    private int Qtd;

    //Construtor da classe Produto
    public Produto2(String Nome, double Preco, int Qtd) {

        this.Nome = Nome;
        this.preco = Preco;
        this.Qtd = Qtd;
    }

    // metodo setNome
    public String setNome(String Nome) {
        this.Nome = Nome;
        return Nome;

    }

    // metodo getNome
    public String getNome() {
        return Nome;
    }

    // metodo setPreço
    public double setPreco(double Preco) {
        this.preco = Preco;
        return Preco;

    }

    // metodo getPreço
    public double getPreco() {
        return preco;
    }

    // metodo setQtd
    public int setQtd(int Qtd) {
        this.Qtd = Qtd;
        return Qtd;

    }

    // metodo getQtd
    public int getQtd() {
        return Qtd;
    }

    // Método para aumentar a quantidade do produto
    public void AumentarQtd(int Qtd) {
        this.Qtd += Qtd;
    }

    // Método para diminuir a quantidade do produto
    public void DiminuirQtd(int Qtd) {
        if (this.Qtd >= Qtd) {
            this.Qtd -= Qtd;
        } else {
            System.out.println("Quantidade insuficiente em estoque.");
        }
    }
}


