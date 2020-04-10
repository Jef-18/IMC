# IMC
# Calcular IMC do(a) usuário(a).

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Aula1
{
    public partial class Form1 : Form
    {
        //variáveis
        double peso, altura, imc;

        public Form1()
        {
            InitializeComponent();
        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void txtCalcular_Click(object sender, EventArgs e)
        {
            //coverter
            peso   = Convert.ToDouble(txtBoxPeso.Text);
            altura = Convert.ToDouble(txtBoxAltura.Text);

            //calcular
            imc    =  peso / (altura * altura);

            //resultado
            if (imc < 18.5)
            {
                MessageBox.Show("Peso abaixo do normal. " + "Seu IMC é: " + Math.Round(imc, 2));
            }
            else if (imc < 25)
            {
                MessageBox.Show("Peso normal. " + "Seu IMC é: " + Math.Round(imc, 2));
            }
            else if (imc < 30)
            {
                MessageBox.Show("Sobrepeso. " + "Seu IMC é: " + Math.Round(imc, 2));
            }

            else if (imc > 30)
            {
                MessageBox.Show("Obesidade. " + "Seu IMC é: " + Math.Round(imc, 2));
            }

            Console.Read();

        }
    }
}



