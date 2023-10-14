# Classe Triangle

A classe Triangle representa um triângulo e contém métodos para calcular sua área, perímetro, altura e tipo. Ele também pode exibir os dados do triângulo em HTML, JSON e em txt.

# Construtores
A classe Triangle possui um construtor que recebe três parâmetros, que representam os comprimentos dos lados do triângulo. Esses valores devem ser números reais positivos e representar os comprimentos de lados diferentes.

Se algum dos lados for menor ou igual a zero, ou se a soma de dois lados for menor ou igual ao terceiro lado, a classe lançará uma exceção IllegalArgumentException.

# Métodos
A classe Triangle possui os seguintes métodos:

getSide1(), getSide2(), getSide3()
Retorna os comprimentos dos lados do triângulo.

getPerimeter()
Calcula e retorna o perímetro do triângulo, que é a soma dos comprimentos dos três lados do triängulo.

getArea()
Calcula e retorna a área do triângulo usando a fórmula de Heron.

getHeight()
Calcula e retorna a altura do triângulo em relação ao maior lado.

getType()
Determina e retorna o tipo do triângulo, que pode ser Equilateral (todos os lados iguais), Isosceles (dois lados iguais) ou Scalene (nenhum lado igual).

toHtml()
Retorna uma string contendo a representação HTML do triângulo, com cada dado em uma linha separada.

toJson()
Retorna uma string contendo a representação JSON do triângulo.

toTxt()
Retorna uma string contendo a representação em texto do triângulo, com cada dado em uma linha separada.

# Exemplo de uso
Aqui está um exemplo de como usar a classe Triangle:

````java
Triangle triangle = new Triangle(3.0, 4.0, 5.0);
System.out.println(triangle.getArea()); // Saída: 6.0
System.out.println(triangle.getPerimeter()); // Saída: 12.0
System.out.println(triangle.getHeight()); // Saída: 4.0
System.out.println(triangle.getType()); // Saída: Scalene
System.out.println(triangle.toHtml()); // Saída: <ul><li>Side 1: 3.0</li><li>Side 2: 4.0</li><li>Side 3: 5.0</li><li>Perimeter: 12.0</li><li>Area: 6.0</li><li>Height: 4.0</li><li>Type: Scalene</li></ul>
System.out.println(triangle.toJson()); // Saída: {"side1": 3.0, "side2": 4.0, "side3": 5.0, "perimeter": 12.0, "area": 6.0, "height": 4.0, "type": "Scalene"}
System.out.println(triangle.toTxt()); // Saída: Triangle\nSide 1: 3.0\nSide 2: 4.0\nSide 3: 5.0\nPerimeter: 12.0\nArea: 6.0\nHeight: 4.0\nType: Scalene\n

````