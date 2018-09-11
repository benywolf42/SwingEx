# SwingEx01

package com.company;

import javax.swing.JOptionPane;

public class Main {
    static int[] sexo = new int[10];
    static int[] idadeConvertida = new int[10];
    static int[] satisfacaoCliente = new int[10];
    static int contMasc = 0;
    static int contFem = 0;
    static int contSim = 0;
    static int contNao = 0;

    public static void main(String[] args) {

        exibirMensagens();
        contagemSexo();
        contagemSimNao();
        exibirRespostas();

    }

    public static void exibirMensagens() {
        for (int i = 0; i < 10; i++) {
            sexo[i] = JOptionPane.showConfirmDialog( // se 0, sim; se 1, não.
                    null, "Você é do sexo feminino?",
                    "Sexo", JOptionPane.YES_NO_OPTION, JOptionPane.QUESTION_MESSAGE);

            String idade = JOptionPane.showInputDialog(null, "Digite a sua idade",
                    "Idade", JOptionPane.QUESTION_MESSAGE);
            idadeConvertida[i] = Integer.parseInt(idade); // convertendo a string em int

            satisfacaoCliente[i] = JOptionPane.showConfirmDialog( // se 0, sim; se 1, não.
                    null, "Você gostou do nosso produto?",
                    "Satisfação do cliente", JOptionPane.YES_NO_OPTION, JOptionPane.QUESTION_MESSAGE);
        }
    }

    public static void contagemSexo(){
        for (int i = 0; i < 10; i++) {
            if (sexo[i] != 0)
                contMasc += 1;
            else
                contFem += 1;
        }

    }

    public static void contagemSimNao(){
        for (int i = 0; i < 10; i++) {
            if (satisfacaoCliente[i] != 0)
                contNao += 1;
            else
                contSim += 1;
        }
    }

    public static void exibirRespostas(){
        JOptionPane.showMessageDialog(null,
                "Quantidade de pessoas do sexo masculino: " + contMasc
                +"\nQuantidade de pessoas do sexo feminino: " + contFem
                +"\nQuantidade de pessoas que disseram sim: " + contSim
                +"\nQuantidade de pessoas que disseram não: " + contNao,
                null,
                JOptionPane.INFORMATION_MESSAGE
        );
    }
}

=========================================================================

#SwingEx02

package com.company;

import javax.swing.JOptionPane;

public class Main {
    static String[] nome = new String[5];

    public static void main(String[] args) {
        for (int i = 0; i < 5; i++) {
            nome[i] = JOptionPane.showInputDialog(null, "Digite o seu nome completo",
                    "Nome completo", JOptionPane.QUESTION_MESSAGE);

        }

        for (int i = 4; i >= 0; i--) {
            System.out.println("Nome do usuário número " + i + ": " + nome[i]);
            JOptionPane.showMessageDialog(null,
                    "Nome do usuário número " + (i+1) + ": " + nome[i],
                    null,
                    JOptionPane.WARNING_MESSAGE);
        }
    }
}
=========================================================================

#SwingEx03
