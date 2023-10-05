Console.WriteLine("enter a :");
int a = int.Parse(Console.ReadLine());
Console.WriteLine("enter b :");
int b = int.Parse(Console.ReadLine());
int c;
string str = "";
Console.WriteLine("prime num : ");
for (int i = a + 1; i < b; i++)
{
    c = 0;
    for (int j = 2; j < i; j++)
    {
        if (i % j == 0)
        {
            c++;
        }
    }
    if (c == 0)
    {
        if (str != "")
        {
            str += ", ";
        }
        str += i;
    }


   
}
Console.WriteLine(str);
Console.WriteLine("mirror nums : ");

for(int i =a ; i < b; i++)
{
    if (pal(i))
    {
        Console.WriteLine(i);
    }
}
static bool pal(int num)
{
    int re = 0, tem, remin;
    tem = num;
    while(num!=0)
    {
        remin = num % 10;
        re = re * 10 + remin;
        num = num / 10;
    }
    return tem ==re;
}
Console.ReadLine(); 
