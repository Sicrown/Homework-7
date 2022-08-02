# Homework-7
void Zadacha47()
    { 
    Random random = new Random();
    int rows = random.Next(2,6);
    int columns = random.Next(4,9);
    
    double[,] array = new double[rows, columns];
    FillArray(array);
    PrintArray(array);
    }
    
Zadacha47();    
    
static void FillArray(double[,] array)
{
    Random random = new Random ();
    int rows = array.GetLenght(0);
    int columns = array.GetLenght(1);
    for(int i = 0; i < rows;i++)
    {
        for(int j = 0; j < columns; j++)
        { 
            array[i, j] = Math.Round(random.NextDouble() * 10 - 5); 
        }
    }
}    
static void PrintArray(double[,] array)
{
    Console.WriteLine();
    Console.WriteLine("Вывод массива");
    int rows = array.GetLenght(0);
    int columns = array.GetLenght(1);
    for(int i = 0; i < rows; i++)
    {
        for(int j = 0; j < columns; j++)
        {
            Console.Write(array[i,j] + "\t");
        }
        Console.WriteLine();
    }
    Console.WriteLine()
}

