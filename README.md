# ClasseTeste
Usando a classe de teste para testar uma classe chamada conversor no Apex


public class ConversorEXCNana {
    public static Decimal CelsiusParaFahrenheit(Decimal celsius){
        return (celsius * 9/5) + 32;


    }
    public static Decimal FahrenheitParaCelsius(Decimal Fahrenheit){
        Decimal fh = (Fahrenheit-32) * 5/9;
        return fh.setScale(2);

    }
    public static Decimal KelvinParaCelcius(Decimal Kelvin){
        return (Kelvin-273.15);

    }
    public static Decimal MetroParaCm(Decimal Metro){
        return (Metro * 100);
    }
    

}

