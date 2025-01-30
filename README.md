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
        }int ContarCaracter(string texto, char caracter)
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
