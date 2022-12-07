# Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна трем символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

## Примеры: 
["hello", "2", "world", ":-)"] -> ["2", ":-)"] ["1234", "1567", "-2", "computer science"] -> ["-2"] ["Russia", "Denmark", "Kazan"] -> []

## Выполнение задачи
Создаем массив:
```
void PrintArray(string[] inArray)

{
    for (int i = 0; i < inArray.GetLength(0); i++)
    {
        Console.Write($"{inArray[i] + " "}");
    }
}
```

Запрашиваем ввод элементов, поочередно вводим элементы в массив строк
```
Console.Write("Введите необходимое количество элементов: ");
int size = int.Parse(Console.ReadLine()!);

string[] arrayStrings = new string[size];
for (int i = 0; i < size; i++)
{
    Console.WriteLine($"Введите {i + 1}-й элемент: ");         
    string element = Convert.ToString(Console.ReadLine());
    arrayStrings[i] = element;
}
```
