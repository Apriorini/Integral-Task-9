Console.WriteLine("Введите нижний предел а");
double a = Convert.ToDouble(Console.ReadLine());
Console.WriteLine("Введите верхний предел b");
double b = Convert.ToDouble(Console.ReadLine());
Console.WriteLine("Введите количество разбиений интеграла n");
double n = Convert.ToDouble(Console.ReadLine());
if (n <= 0)
{
    Console.WriteLine("Ошибка: n должно быть положительным целым числом");
    return;
}
double h = (b - a) / n;
double sum = 0;
for (int i = 1; i <= n; i++)
{
    sum += a + i * h / 2;
}
double x = h * sum;
double integral = 2 * Math.Pow(x, 2) + 3 * x;
Console.WriteLine($"Ответ - {integral}");
