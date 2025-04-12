# Projeto-Java-atividades-

// Classe base (superclasse)
class Animal {
    // Atributos comuns a todos os animais
    protected String nome;
    protected int idade;
    protected String especie;

    // Construtor da classe base
    public Animal(String nome, int idade, String especie) {
        this.nome = nome;
        this.idade = idade;
        this.especie = especie;
    }

    // Método comum a todos os animais
    public void mostrarInformacoes() {
        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade + " anos");
        System.out.println("Espécie: " + especie);
    }

    // Método que será sobrescrito
    public void fazerSom() {
        System.out.println("Este animal faz um som.");
    }

    // Método que será sobrescrito
    public void alimentar() {
        System.out.println("Alimentando o animal.");
    }
}

// Classe derivada (subclasse) - Herança
class Leao extends Animal {

    // Construtor da subclasse
    public Leao(String nome, int idade) {
        super(nome, idade, "Leão");  // Chama o construtor da superclasse
    }

    // Sobrescreve o método fazerSom da classe base
    @Override
    public void fazerSom() {
        System.out.println("O leão ruge: ROAARRR!");
    }

    // Sobrescreve o método alimentar da classe base
    @Override
    public void alimentar() {
        System.out.println("Alimentando o leão com carne.");
    }
}

// Outra classe derivada (subclasse) - Herança
class Elefante extends Animal {

    // Construtor da subclasse
    public Elefante(String nome, int idade) {
        super(nome, idade, "Elefante");  // Chama o construtor da superclasse
    }

    // Sobrescreve o método fazerSom da classe base
    @Override
    public void fazerSom() {
        System.out.println("O elefante faz um barulho: PAAAARRRR!");
    }

    // Sobrescreve o método alimentar da classe base
    @Override
    public void alimentar() {
        System.out.println("Alimentando o elefante com feno e frutas.");
    }
}

// Outra classe derivada (subclasse) - Herança
class Passaro extends Animal {

    // Construtor da subclasse
    public Passaro(String nome, int idade) {
        super(nome, idade, "Pássaro");  // Chama o construtor da superclasse
    }

    // Sobrescreve o método fazerSom da classe base
    @Override
    public void fazerSom() {
        System.out.println("O pássaro canta: Fiu-fiu!");
    }

    // Sobrescreve o método alimentar da classe base
    @Override
    public void alimentar() {
        System.out.println("Alimentando o pássaro com sementes.");
    }
}

// Classe principal para testar o código
public class TesteZoologico {

    public static void main(String[] args) {
        // Criando objetos dos tipos Leão, Elefante e Pássaro
        Animal leao = new Leao("Simba", 5);
        Animal elefante = new Elefante("Dumbo", 10);
        Animal passaro = new Passaro("Tweety", 2);

        // Mostrando informações gerais
        System.out.println("Informações do Leão:");
        leao.mostrarInformacoes();  // Mostra informações do Leão
        leao.fazerSom();            // Chama o método sobrescrito de fazerSom
        leao.alimentar();           // Chama o método sobrescrito de alimentar

        System.out.println("\nInformações do Elefante:");
        elefante.mostrarInformacoes();  // Mostra informações do Elefante
        elefante.fazerSom();            // Chama o método sobrescrito de fazerSom
        elefante.alimentar();           // Chama o método sobrescrito de alimentar

        System.out.println("\nInformações do Pássaro:");
        passaro.mostrarInformacoes();   // Mostra informações do Pássaro
        passaro.fazerSom();             // Chama o método sobrescrito de fazerSom
        passaro.alimentar();            // Chama o método sobrescrito de alimentar
    }
}
