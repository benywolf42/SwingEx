# SwingEx01

package com.company;

import javax.swing.JOptionPane;

public class Main {
    static int[] sexo = new int[10];
    static int[] idadeConvertida = new int[10];
    static int[] satisfacaoCliente = new int[10];

    public static void main(String[] args) {

        exibirMensagens();
        contagemSexo();
        contagemSimNao();

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
        int contMasc = 0;
        int contFem = 0;
        for (int i = 0; i < 10; i++) {
            if (sexo[i] != 0)
                contMasc += 1;
            else
                contFem += 1;
        }

        System.out.println("Quantidade de pessoas do sexo masculino: " + contMasc);
        System.out.println("Quantidade de pessoas do sexo feminino: " + contFem);
    }

    public static void contagemSimNao(){
        int contSim = 0;
        int contNao = 0;
        for (int i = 0; i < 10; i++) {
            if (satisfacaoCliente[i] != 0)
                contNao += 1;
            else
                contSim += 1;
        }
        System.out.println("Quantidade de pessoas que disseram sim: " + contSim);
        System.out.println("Quantidade de pessoas que disseram não: " + contNao);
    }
}


=============================================================================================

#SwingEx02


