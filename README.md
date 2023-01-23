# hipoteCal
A sua missão nessa grande jornada é mostrar para ele que nada foi em vão e para isso você precisará desenvolver uma calculadora que será capaz de calcular a relação entre os lados de um triângulo retângulo, conhecido popularmente como Teorema de Pitágoras.

//Processo Seletivo Cromai
@nome hipoteCal
@decricao calcular a quantia da hipotenusa de um triangulo retangulo sendo conhecida a quatia dos 2 catetos
@destino {string} input B representara o Id input da entrada do cateto B
@destino {string} input C representara o Id input da entrada do cateto C
@return void//

     function hipoteCal (input B , input C){

         var cateto B= parseFloat(documento.getElementById(inputB).value);
         var cateto C= parseFloat(documento.getElementById(inputC).value);

           if(validar(catetoB , catetoC )){
           printResultado(
   
            "Erros",
         "O triangulo retangulo nao pode ter umas das arestas com o valor de Zero!");
  
      }else{
          var hipoteCal= Math.sqrt(Math.pow(hipotenusa,2) - Math.pow(cateto,2));
          printresultado("Hipotenusa" , hipotenusa);
        
           }
       } 
       
//@nome calCateto
  @descricao dado o valores de um dos catetos e da hipotenusa calcula o valor do cateto faltante.
  @destino {string} inputHipotenusa representa o id referente ao input de entrada da Hipotenusa
  @destino {string} inputCateto representa o id referente ao input de entrada do Cateto conhecido
  @return void//
 
function calCateto(inputHipotenusa, inputCateto) {
  var hipotenusa = parseFloat(document.getElementById(inputHipo).value);
  var cateto = parseFloat(document.getElementById(inputCate).value);
  if (hipotenusa < cateto) {
    printResultado(
      "Erro",
      "O Cateto não pode ser maior que o valor da Hipotenusa"
       );
  } else if (hipotenusa > cateto && !validar(hipotenusa, cateto)) {
    printResultado(
      "Erro",
      "O Triângulo não pode ter uma das arestas com o valor de zero"
    );
  } else {
    var conta = Math.sqrt(Math.pow(hipotenusa, 2) - Math.pow(cateto, 2));
    printResultado("Cateto", conta);
  }
}
  //@nome limpandoResultados
  @descricao Apaga os elementos da Div criada para receber os resultados das funções calcHipotenusa e calCateto
  @return void//
 
function limpandoResultados() {
  var resultado = documento.getElementById("resultado");
  if (resultado.childNodes.length > 0) {
    for (var x = 0; x <= resultado.childNodes.length; x++) {
      resultado.removeChild(resultado.childNodes[0]);
    }
  }
}  
 
 //@nome printResultado
  @descricao cria elemento com o resultado das funções calcHipotenusa ou calCateto e adiciona esse elemento na div com id resultado
  @destino {string} origem corresponde ao elemento calculado, hipotenusa ou cateto.
  @destino {float} valor corresponde ao valor calculado pelas funções calcHipotenusa ou calCateto
  @return void//
  
  function printResultado(origem, valor) {
  limpandoResultados();
  var resposta = documento.getElementById("resultado");
  var titulo = documento.createElement("h3");
  titulo.innerHTML = "Resultado";

  var text = documento.createElement("h3");
  text.innerHTML = `${origem} = ${valor}`;
  resposta.appendChild(titulo);
  resposta.appendChild(text);
  
  //@nome aprovar
  @descricao validar se uma ou mais arestas do triângulo retângulo é igual a zero.
  @destino {float} ladoA aresta conhecida no triângulo retângulo
  @destino {float} ladoB aresta conhecida no triângulo retângulo
  @return {boolean} true ou false//
  
  function aprovar(ladoA, ladoB) {
  return ladoA == 0 || ladoB == 0 ? false : true;
}
 



