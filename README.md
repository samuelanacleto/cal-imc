package pessoas;

public class pessoa {
	
public String Nome;
public Double Altura;
public Double Peso;
	

pessoa (String Nome,Double Altura, Double Peso){
	this.Nome=Nome;
	this.Altura=Altura;
	this.Peso=Peso;
	
 }
	
public double calcImc (){
    return (this.Peso / (this.Altura*this.Altura) );
    
	
}
public String resultadoIMC()
{
	String result;
	double imc = this.calcImc();
	
	if (imc <=18)
		result = "abaixo do peso";
	else if (imc <=28)
		result = "peso ideal";
	else if (imc <=30)
		result = "acima do peso";
	else if (imc <=35)
        result= "Obesidade leve";
	else 
		result = "Obesidade";
	return result;
}}
/////////////////////////////////////////////////////////////////////////////////////////////
#test
package pessoas;

import java.text.DecimalFormat;

public class teste {
	
	public static void main(String[] args) {
	DecimalFormat df = new DecimalFormat(".##");
	pessoa a1 = new pessoa ("joao",1.80,90.00);
     
    System.out.println("imc:" +df.format(a1.calcImc()));
    System.out.print("imc:" +a1.resultadoIMC());
}}
 
