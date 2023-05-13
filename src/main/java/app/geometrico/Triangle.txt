package app.geometrico;

public class Triangle {
    private double side1;
    private double side2;
    private double side3;

    public Triangle(double side1, double side2, double side3) {
        this.side1 = side1;
        this.side2 = side2;
        this.side3 = side3;
    }

    public double getSide1() {
        return side1;
    }

    public double getSide2() {
        return side2;
    }

    public double getSide3() {
        return side3;
    }

    public double getPerimeter() {
        return side1 + side2 + side3;
    }

    public double getArea() {
        double p = getPerimeter() / 2.0;
        return Math.sqrt(p * (p - side1) * (p - side2) * (p - side3));
    }

    public double getHeight() {
        return (2 * getArea()) / side1;
    }

    public String getType() {
        if (side1 == side2 && side2 == side3) {
            return "Equilateral";
        } else if (side1 == side2 || side1 == side3 || side2 == side3) {
            return "Isosceles";
        } else {
            return "Scalene";
        }
    }

    public String toHtml() {
        String html = "<p>Triangle</p><ul>"
                + "<li>Side 1: " + side1 + "</li>"
                + "<li>Side 2: " + side2 + "</li>"
                + "<li>Side 3: " + side3 + "</li>"
                + "<li>Perimeter: " + getPerimeter() + "</li>"
                + "<li>Area: " + getArea() + "</li>"
                + "<li>Height: " + getHeight() + "</li>"
                + "<li>Type: " + getType() + "</li>"
                + "</ul>";
        return html;
    }

    public String toJson() {
        String json = "{"
                + "\"side1\": " + side1 + ","
                + "\"side2\": " + side2 + ","
                + "\"side3\": " + side3 + ","
                + "\"perimeter\": " + getPerimeter() + ","
                + "\"area\": " + getArea() + ","
                + "\"height\": " + getHeight() + ","
                + "\"type\": \"" + getType() + "\""
                + "}";
        return json;
    }

    public String toTxt() {
        String txt = "Triangle\n"
                + "Side 1: " + side1 + "\n"
                + "Side 2: " + side2 + "\n"
                + "Side 3: " + side3 + "\n"
                + "Perimeter: " + getPerimeter() + "\n"
                + "Area: " + getArea() + "\n"
                + "Height: " + getHeight() + "\n"
                + "Type: " + getType() + "\n";
        return txt;
    }
}
