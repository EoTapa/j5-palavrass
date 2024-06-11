# j5-palavrass

let palavra; 

function setup() {
  createCanvas(400, 400);
  
  palavra = palavraAleatoria();
}

function palavraAleatoria(){
  
  let palavras = ["caminhante", "caminho","caminha"];

return random(palavras);
}

function inicializaCore(){
  background("white")
fill ("black");
  textSize(64);
  textAlign(CENTER, CENTER);
}

function palavraParcial(minimo, maximo){
  let quantidade = map(mouseX, minimo, maximo, 1, palavra.length);
let parcial = palavra.substring(0, quantidade);
  return parcial;
}

function draw(){
  inicializaCore();
let texto = palavraParcial(0, width);
  text(texto, 200, 200);
}

function modoNortuno(horario) {
  if (horario>18){
    console.log("você precisa ligar o modo escuro!");
  } else {
    console.log("modo nortuno não é necessario neste momento.");
  }
}

