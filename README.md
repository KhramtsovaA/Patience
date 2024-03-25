// Задайте массив. Напишите программу, которая определяет,
// присутствует ли заданное число в массиве. Программа
// должна выдать ответ: Да/Нет.
// Примеры
// [1 3 4 19 3], 8 => Нет
// [-4 3 4 1], 3 => Да 


System.Console.WriteLine("Введите размер массива:");
int arraySize = Convert.ToInt32(Console.ReadLine());
int[] myArray = new int[arraySize];
Random rand = new Random();

for (int i = 0; i < myArray.Length; i++)
{
    myArray[i] = rand.Next(0, 10);
}

for (int i = 0; i < myArray.Length; i++)
{
    System.Console.Write(myArray[i] + " ");
}
System.Console.Write("\nВведите искомое число: ");
int number = Convert.ToInt32(Console.ReadLine());

bool numberisFinded = false;

for (int i = 0; i < myArray.Length; i++)
{
    if (myArray[i] == number)
    {
        numberisFinded = true;
        break;
    }
}
if (numberisFinded)
{
    System.Console.WriteLine("Да");
}
else
{
    System.Console.WriteLine("Нет");
}

