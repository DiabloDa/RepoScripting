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
### 7. MAtriz
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
