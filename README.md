# ClasseTeste
Usando a Classe de Teste para testar uma Classe chamada Conversor no Apex








### Classe Conversor

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


   ### Classe de Teste

    @isTest
    public class ConversorEXCNanaTest {
    @isTest public static void TestCelsiusParaFahrenheit(){
        Decimal celsius1 = ConversorEXCNana.CelsiusParaFahrenheit(50);
       System.assertEquals(122, celsius1, 'Resultado não esperado');
        
    }
    @isTest public static void TestFahrenheitParaCelsius(){
        Decimal Fahrenheit1 = ConversorEXCNana.FahrenheitParaCelsius(80);
        System.assertEquals(24, Fahrenheit1 , 'Resultado não esperado');
    }
    @isTest public static void TestKelvinParaCelcius(){
        Decimal Kelvin1 = ConversorEXCNana.KelvinParaCelcius(500);
        System.assertEquals(24, Kelvin1 , 'Resultado não esperado');
    }
     @isTest public static void TestMetroParaCm(){
        Decimal Metro1 = ConversorEXCNana.MetroParaCm(5);
        System.assertEquals(500, Metro1 , 'Resultado não esperado');
     }

}

