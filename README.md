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
### 5. Con multiples parametro
```csharp
double CalcularPromedio(double num1, double num2, double num3)
{
    return (num1 + num2 + num3) / 3;
}
Console.WriteLine(CalcularPromedio(4.5, 3.2, 6.7));
```
