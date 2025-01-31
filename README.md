# 4. Firmas
### 1. Sin parametro, sin retorno
```csharp
void Saludar()
{
    Console.WriteLine("Holi");
}
Saludar();
```
### 2. Con parametro
```csharp
void MostrarMensaje(string mensaje)
{
    Console.WriteLine(mensaje);
}
MostrarMensaje("WOWOWOWOW");
```
### 3. Con retorno
```csharp
int Sumar(int a, int b)
{
    return a + b;
}
int resultado = Sumar(2, 1);
Console.WriteLine(resultado); 
```
### 4. Con multiples parametro
```csharp
double CalcularPromedio(double num1, double num2, double num3)
{
    return (num1 + num2 + num3) / 3;
}
Console.WriteLine(CalcularPromedio(4.5, 3.2, 6.7));
```
### 5. Con Array
```csharp
int SumarElementos(int[] numeros)
{
    int suma = 0;
    foreach (int num in numeros)
    {
        suma += num;
    }
    return suma;
}

int[] arreglo = { 1, 2, 3, 4 };
Console.WriteLine(SumarElementos(arreglo));
```
### 6. Con Lista
```csharp
void ImprimirLista(List<string> nombres)
{
    foreach (var nombre in nombres)
    {
        Console.WriteLine(nombre);
    }
}
List<string> nombres = new List<string> { "Juan", "María", "Pedro" };
ImprimirLista(nombres);
```
### 7. Con parametros cambiables
```csharp
void MostrarSaludo(string nombre = "Invitado")
{
    Console.WriteLine($"Hola, {nombre}!");
}
MostrarSaludo();
Console.WriteLine("Dime tu nombre pls");
string nombre = Convert.ToString(Console.ReadLine()); 
MostrarSaludo(nombre); 
Console.ReadLine();
```
### 7. Matriz
```csharp
void CrearYMostrarMatriz(int filas, int columnas)
    {
        int[,] matriz = new int[filas, columnas];

        int numero = 1;
        for (int i = 0; i < filas; i++)
        {
            for (int j = 0; j < columnas; j++)
            {
                matriz[i, j] = numero++;
            }
        }

        Console.WriteLine("La matriz generada es:");
        for (int i = 0; i < filas; i++)
        {
            for (int j = 0; j < columnas; j++)
            {
                Console.Write(matriz[i, j] + "\t");
            }
            Console.WriteLine();
        }
    }
Console.WriteLine("Ingresa el número de filas:");
        int filas = int.Parse(Console.ReadLine());
        
        Console.WriteLine("Ingresa el número de columnas:");
        int columnas = int.Parse(Console.ReadLine());

        CrearYMostrarMatriz(filas, columnas);
```
### 8. Par o Impar
```csharp
bool EsPar(int numero)
{
    return numero % 2 == 0;
}
Console.WriteLine("Ingresa un número:");
int numero = int.Parse(Console.ReadLine());

if (EsPar(numero))
Console.WriteLine("El número es par.");
else
Console.WriteLine("El número es impar.");
```
### 9. Radio de un circulo
```csharp
double CalcularAreaCirculo(double radio)
{
     return Math.PI * Math.Pow(radio, 2);
}

Console.WriteLine("Ingresa el radio del círculo:");
            double radio = double.Parse(Console.ReadLine());

            double area = CalcularAreaCirculo(radio);
            Console.WriteLine("El área del círculo es: " + area);
            Console.ReadLine();
```
### 10. Radio de un circulo
```csharp
int EncontrarMaximo(int num1, int num2, int num3)
{
    int maximo = num1;

    if (num2 > maximo)
        maximo = num2;
    if (num3 > maximo)
        maximo = num3;

    return maximo;
}

Console.WriteLine("Ingresa tres números:");

    Console.Write("Número 1: ");
    int num1 = int.Parse(Console.ReadLine());

    Console.Write("Número 2: ");
    int num2 = int.Parse(Console.ReadLine());

    Console.Write("Número 3: ");
    int num3 = int.Parse(Console.ReadLine());

    int maximo = EncontrarMaximo(num1, num2, num3);
    Console.WriteLine("El número mayor es: " + maximo);
```
### 11. + o - o 0
```csharp
void VerificarNumero(int numero)
{
    if (numero > 0)
        Console.WriteLine("El numero es positivo.");
    else if (numero < 0)
        Console.WriteLine("El numero es negativo.");
    else
        Console.WriteLine("El numero es cero.");
}
Console.WriteLine("Ingresa un número:");
    int numero = int.Parse(Console.ReadLine());

    VerificarNumero(numero);
```
### 12. Contador de letras
```csharp
vint ContarCaracter(string texto, char caracter)
        {
            int contador = 0;

            foreach (char c in texto)
            {
                if (c == caracter)
                    contador++;
            }

            return contador;
        }
Console.WriteLine("Ingresa una cadena de texto:");
            string texto = Console.ReadLine();

            Console.WriteLine("Ingresa el carácter a contar:");
            char caracter = char.Parse(Console.ReadLine());

            int cantidad = ContarCaracter(texto, caracter);
            Console.WriteLine("El carácter " + caracter + " aparece " +cantidad+ " veces.");
            Console.ReadLine();
```
### 13. Promedio de un arreglo
```csharp
double CalcularPromedio(int[] numeros)
        {
            int suma = 0;
            foreach (int num in numeros)
            {
                suma += num;
            }
            return suma / (double)numeros.Length;
        }
Console.WriteLine("Ingresa el número de elementos:");
            int cantidad = int.Parse(Console.ReadLine());

            int[] numeros = new int[cantidad];

            for (int i = 0; i < cantidad; i++)
            {
                Console.WriteLine("Ingresa el número "+ (i+1) +":");
                numeros[i] = int.Parse(Console.ReadLine());
            }

            double promedio = CalcularPromedio(numeros);
            Console.WriteLine("El promedio es: " + promedio);
            Console.ReadLine();
```
### 14. Cuenta regresiva
```csharp
void ImprimirNumeros(int N)
        {
            for (int i = N; i >= 0; i--)
            {
                Console.WriteLine(i);
            }
        }
 Console.WriteLine("Ingresa un número N:");
    int N = int.Parse(Console.ReadLine());
    ImprimirNumeros(N);
```
### 15. Con cadenas
```csharp
string InvertirCadena(string texto)
{
    char[] caracteres = texto.ToCharArray();  
    Array.Reverse(caracteres);  
    return new string(caracteres);  
}
Console.WriteLine("Ingresa una cadena para invertir:");
            string texto = Console.ReadLine();
            string textoInvertido = InvertirCadena(texto);
            Console.WriteLine($"La cadena invertida es: "+ textoInvertido);
            Console.ReadLine();
```
### 16. Con Subcadenas
```csharp
int ContarSubcadena(string texto, string subcadena)
        {
            int contador = 0;
            int posicion = 0;    
            while ((posicion = texto.IndexOf(subcadena, posicion)) != -1)
            {
                contador++;
                posicion += subcadena.Length; 
            }
            return contador;
        }
 Console.WriteLine("Ingresa una cadena:");
            string texto = Console.ReadLine();
            Console.WriteLine("Ingresa la subcadena a buscar:");
            string subcadena = Console.ReadLine();
            int cantidad = ContarSubcadena(texto, subcadena);
            Console.WriteLine("La subcadena "+ subcadena +" aparece "+ cantidad+ " veces en el texto.");
```
### 17. Con cadenas
```csharp
string InvertirCadena(string texto)
{
    char[] caracteres = texto.ToCharArray();  
    Array.Reverse(caracteres);  
    return new string(caracteres);  
}
Console.WriteLine("Ingresa una cadena para invertir:");
            string texto = Console.ReadLine();
            string textoInvertido = InvertirCadena(texto);
            Console.WriteLine($"La cadena invertida es: "+ textoInvertido);
            Console.ReadLine();
```
### 18. Transpuesta de una matriz
```csharp
int[,] TransponerMatriz(int[,] matriz)
{
    int filas = matriz.GetLength(0);
    int columnas = matriz.GetLength(1);
    int[,] transpuesta = new int[columnas, filas];

    for (int i = 0; i < filas; i++)
    {
        for (int j = 0; j < columnas; j++)
        {
            transpuesta[j, i] = matriz[i, j];
        }
    }

    return transpuesta;
}
int[,] matriz = {
        { 1, 2, 3 },
        { 4, 5, 6 }
    };

    int[,] transpuesta = TransponerMatriz(matriz);

    Console.WriteLine("Matriz transpuesta:");
    for (int i = 0; i < transpuesta.GetLength(0); i++)
    {
        for (int j = 0; j < transpuesta.GetLength(1); j++)
        {
            Console.Write(transpuesta[i, j] + " ");
        }
        Console.WriteLine();
    }
```
### 19. Intercambios
```csharp
void Intercambiar(ref int a, ref int b)
{
    a = a + b;  
    b = a - b;  
    a = a - b;  
}
    int a = 5, b = 10;
    Console.WriteLine("Antes del intercambio: a = "+a+", b ="+b);
    Intercambiar(ref a, ref b);
    Console.WriteLine($"Después del intercambio: a = "+a+", b ="+b);
```
### 20. Mismos números
```csharp
List<int> ObtenerElementosComunes(List<int> lista1, List<int> lista2)
{
    List<int> comunes = new List<int>();
    foreach (var item in lista1)
    {
        if (lista2.Contains(item))
        {
            comunes.Add(item);
        }
    }
    return comunes;
}
    List<int> lista1 = new List<int> { 1, 2, 3, 4, 5 };
    List<int> lista2 = new List<int> { 4, 5, 6, 7, 8 };
    List<int> comunes = ObtenerElementosComunes(lista1, lista2);
    Console.WriteLine("Elementos comunes:");
    foreach (var item in comunes)
    {
        Console.Write(item + " ");
    }
```

## Ejercicio de ciclos (6)

```csharp
using System.Linq.Expressions;
using System.Security.Cryptography.X509Certificates;

namespace Talller_1_Scrpting_ejercicio_2
{
    internal class Program
    {
        static void Main(string[] args)
        {

            Ciclo();
            

        }
        public static void Ciclo()
        {
            int tamaño = 0;
            Console.WriteLine("Por favor ingrese el número hasta que desea sumar");
            tamaño = Convert.ToInt32(Console.ReadLine());
            int suma = 0;
            int contador = 0;
            int numero = 1;
            
            do
            {

                suma += numero;
                contador++;
                numero += 2;

            } while (contador < tamaño);

            Console.WriteLine($"La suma de los primeros {tamaño} números impares es: {suma}");
        }
    }
}

```

## Actividad Función
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Runtime.InteropServices;
using System.Text;
using System.Threading.Tasks;

namespace EjercicioFunción
{
    internal class Program
    {
        public static List<string> rSandwich = new List<string>();
        static void Main(string[] args)
        {
            Menu();
        }

        public static void Menu()
        {
            int respuesta = 0;
            Console.WriteLine("Escribe el número de la forma quieres hacer el sandwich");
            Console.WriteLine("1. Función  2. Sin función");
            try
            {
                respuesta = int.Parse(Console.ReadLine());
            }
            catch
            {
                Console.WriteLine("Valor incorrecto");
                Menu();
            }
            if (respuesta == 1)
            {
                Instrucciones();
                string[] ingredientes = Sandwich();
                foreach (var n in ingredientes)
                {
                    Console.WriteLine(n);
                }
                Menu();
            }
            else if(respuesta == 2)
            {
                Console.WriteLine("Escriba el ingrediente, pulse enter, escriba el otro y repita el proceso");
                Console.WriteLine("con la cantidad de ingredientes que desee.");
                Console.WriteLine("Si no va a añadir más pulse X");
                string ing = "";
                bool agregarMas = true;

                while (agregarMas)
                {
                    
                    ing = Console.ReadLine().Trim();

                    if (ing.ToLower() == "x")
                    {
                        agregarMas = false;
                    }
                    else
                    {
                        rSandwich.Add(ing);  // Agregar el ingrediente directamente
                    }
                }

               
                
                foreach (var n in rSandwich)
                {
                    Console.WriteLine(n);
                }

                Console.WriteLine("1");
                Console.WriteLine("2");
                Console.WriteLine("3");
                Console.WriteLine("4");

                Console.WriteLine("Escriba el ingrediente, pulse enter, escriba el otro y repita el proceso");
                Console.WriteLine("con la cantidad de ingredientes que desee.");
                Console.WriteLine("Si no va a añadir más pulse X");
                ing = "";
                agregarMas = true;

                while (agregarMas)
                {
                    Console.WriteLine("Escribe un ingrediente para el sandwich (o 'X' para finalizar): ");
                    ing = Console.ReadLine().Trim();

                    if (ing.ToLower() == "x")
                    {
                        agregarMas = false;
                    }
                    else
                    {
                        rSandwich.Add(ing);  // Agregar el ingrediente directamente
                    }
                }



                foreach (var n in rSandwich)
                {
                    Console.WriteLine(n);
                }

                Console.WriteLine("1");
                Console.WriteLine("2");
                Console.WriteLine("3");
                Console.WriteLine("4");
            }
        }

        public static void Instrucciones()
        {
            Console.WriteLine("Escriba el ingrediente, pulse enter, escriba el otro y repita el proceso");
            Console.WriteLine("con la cantidad de ingredientes que desee.");
            Console.WriteLine("Si no va a añadir más pulse X");
            
        }
        public static string[] Sandwich()
        {
           
            string ing = "";

            ing = Console.ReadLine();

            if (ing.ToLower().Trim() == "x")
            {
                return rSandwich.ToArray();
            }
            else
            {
                rSandwich.Add(ing);
                Sandwich();
            }

            return rSandwich.ToArray();
        }
    }
}

```
## Ejercicio de función 2 (ejercicio 21).
```csharp

using System.Reflection;

namespace Taller1Scripting
{
    internal class Program
    {
        static void Main(string[] args)
        {

            Menu();

        }

        public static void Menu()
        {
            int respuesta;
            Console.WriteLine("Bienvenido al menú");
            Console.WriteLine("Por favor digite el número de la opción del menú que desea elegir");
            Console.WriteLine("-----------Menú----------");
            Console.WriteLine("1)División.     2)Módulo.");
            Console.WriteLine("3)Cuadrado.     3)Negativo.");
            respuesta = int.Parse(Console.ReadLine());

            switch (respuesta)
            {
                case 1:

                    división();

                    break;

                case 2:

                    Modulo();

                    break;

                case 3:

                    Cuadrado();

                    break;

                case 4:

                    Negativo();

                    break;

            }
        }

        public static void Terminar()
        {
            Console.WriteLine("Desea volver la menú o salir");
            Console.WriteLine("Si desea volver al menú digite el número 1");
            Console.WriteLine("Si desea salir presione 2");
            int variable = Convert.ToInt32(Console.ReadLine());

            switch (variable)
            {

                case 1:

                    Menu();

                    break;

                case 2:

                    Console.WriteLine("Graias por utilizar el programa");

                    break;

            }
        }

        public static void división()
        {
            double num1 = 0;
            double num2 = 0;
            double respuesta;

            Console.WriteLine("Por favor ingrese el dividendo");
            num1 = Convert.ToDouble(Console.ReadLine());
            Console.WriteLine("Por favor ingrese el divisor");
            num2 = Convert.ToDouble(Console.ReadLine());

            if (num2 == 0)
            {
                Console.WriteLine("el divisor no puede ser 0");
                Console.WriteLine("por favor vuelva a intentarlo ");
                división();
            }
            else
            {
                respuesta = num1 / num2;
                Console.WriteLine("El resultado de tu división es" + "" + respuesta);
                Terminar();

            }

        }

        public static void Modulo()
        {

            double num1 = 0;
            double num2 = 0;
            double respuesta;

            Console.WriteLine("Por favor ingrese el dividendo");
            num1 = Convert.ToDouble(Console.ReadLine());
            Console.WriteLine("Por favor ingrese el divisor");
            num2 = Convert.ToDouble(Console.ReadLine());

            if (num2 == 0)
            {
                Console.WriteLine("el divisor no puede ser 0");
                Console.WriteLine("por favor vuelva a intentarlo ");
                Modulo();
            }
            else
            {
                respuesta = num1 % num2;
                Console.WriteLine("Este es el residuo de su división" + " " + respuesta);
                Terminar();
            }
            


        }

        public static void Cuadrado()
        {

            double num1 = 0;
            double respuesta;

            Console.WriteLine("Por favor ingrese el número que quiere elevar al cuadrado");
            num1 = Convert.ToDouble(Console.ReadLine());


            respuesta = Math.Pow(num1, 2);
            Console.WriteLine("Este es el resultado del cuadrado" + respuesta);
            Terminar();

        }

        public static void Negativo()
        {

            double num1 = 0;
            double respuesta;

            Console.WriteLine("Por favor ingrese el número que quiere convertir en negativo");
            num1 = Convert.ToDouble(Console.ReadLine());


            respuesta = num1 * -1;
            Console.WriteLine("Este es su nuúmero en negativo" + respuesta);
            Terminar();

        }
    }
}
```

## Ejercicio 15
```csharp
using System;
using System.Collections.Generic;
using System.Data;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Palindroma
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Menu();
        }

        public static void Menu()
        {
            int i = 0;
            Console.WriteLine("Pon una palabra palindroma");
            string palabra = Console.ReadLine();
            i = Verificacion(i, palabra);
            if(i == 1)
            {
                Console.WriteLine("La palabra es palindroma");
            }
            else
            {
                Console.WriteLine("No es palindroma");
            }

        }

        public static int Verificacion(int i, string cadena)
        {
            string palindroma = new string(cadena.ToLower().Reverse().ToArray());

            if(cadena.ToLower() == palindroma)
            {
                i = 1;
            }
            else
            {
                i = 0;
            }
            
            return i;
        }

    }
}

```

## Ejercicio 7
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace PuntoCaracteres
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Menu();
        }
        public static void Menu()
        {
            string num;
            int tamaño;

            Console.WriteLine("Escriba números positivos");
            num = Console.ReadLine();
            tamaño = num.Length;

            int[] numeros = new int[tamaño];

            for (int i = 0; i < tamaño; i++)
            {
                try
                {
                    numeros[i] = int.Parse(num[i].ToString());
                }
                catch
                {
                    Console.WriteLine("Hay un entero");
                }               
            }

            Console.WriteLine("Los números en el array son:");

            foreach (int n in numeros)
            {
                Console.WriteLine(n);
            }
        }
    }
}

```

## Ejercicio 1
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Threading;

namespace MerequetengueSemestre5
{
    internal class Program
    {
        public static int n, m = 0;
        static void Main(string[] args)
        {
            Menu();

        }

        public static void Menu()
        {
            
            Console.WriteLine("Ingrese el tamaño de la matriz");

            try
            {
                n = int.Parse(Console.ReadLine());
                m = int.Parse(Console.ReadLine());
            }

            catch
            {
                Console.WriteLine("Nel, vuelvalo a intentar");
                Menu();
            }

            int[,] matriz = new int[n, m];

            Random rand = new Random();



            for (int i = 0; i < n; i++)
            {
                for (int j = 0; j < m; j++)
                {
                    int numeroAleatorio = rand.Next(-9, 3);
                    matriz[i, j] = numeroAleatorio;
                }
            }

            for (int i = 0; i < n; i++)
            {
                for (int j = 0; j < m; j++)
                {
                    Console.Write("|" + matriz[i, j] + "|");
                }
                Console.WriteLine("");
            }

            Console.WriteLine("Convirtiendo a positivo...");
            Thread.Sleep(1000);
            NumerosPos(matriz);

        }

        public static void NumerosPos(int[,] matriz)
        {
            for (int i = 0; i < n; i++)
            {
                for (int j = 0; j < m; j++)
                {
                    if (matriz[i,j] < 0)
                    {
                        matriz[i, j] = matriz[i, j] * -1; 
                    }
                }
            }

            for (int i = 0; i < n; i++)
            {
                for (int j = 0; j < m; j++)
                {
                    Console.Write("|" + matriz[i, j] + "|");
                }
                Console.WriteLine("");
            }
        }



    }
}

```
