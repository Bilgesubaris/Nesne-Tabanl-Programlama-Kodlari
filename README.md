using System;

class Oyun
{
    private int[,] dizi;

    public Oyun()
    {

        dizi = new int[4, 10];
    }

    public void Yazdır()
    {
        Random random = new Random();

        for (int i = 0; i < dizi.GetLength(0); i++)
        {
            for (int j = 0; j < dizi.GetLength(1); j++)
            {

                dizi[i, j] = random.Next(2);
            }
        }
    }
    class ZorOyun:Oyun
    {
        public  void Seviye(int zorluk)
        {
            Yazdır();
            if (zorluk == 1)
            {
                
                for (int i = 0; i < dizi.GetLength(0); i++)
                {
                    for (int j = 0; j < dizi.GetLength(1) - 1; j++)
                    {
                        if (dizi[i, j] == 0 && dizi[i, j + 1] == 0)
                        {
                            
                            dizi[i, j + 1] = 1;
                        }
                    }
                }
            }
            else if (zorluk == 2)
            {
                
                for (int i = 0; i < dizi.GetLength(0); i++)
                {
                    for (int j = 0; j < dizi.GetLength(1) - 2; j++)
                    {
                        if (dizi[i, j] == 0 && dizi[i, j + 1] == 0 && dizi[i, j + 2] == 0)
                        {
                         
                            dizi[i, j + 2] = 1;
                        }
                    }
                }
            }

        }
    }

    public void MatrisiYazdir()
    {
        for (int i = 0; i < dizi.GetLength(0); i++)
        {
            for (int j = 0; j < dizi.GetLength(1); j++)
            {

                Console.Write(dizi[i, j] == 0 ? "Kırmızı\t" : "Yeşil\t");
            }
            Console.WriteLine();
        }
    }
}

class Program
{
    static void Main()
    {
        
        Console.WriteLine("Zorluk derecesi giriniz: ");
        int a = Convert.ToInt32(Console.ReadLine());
        ZorOyun zorOyun = new ZorOyun(a);


        Oyun oyun = new Oyun();

        oyun.Yazdır();
        Console.WriteLine("Oyun Matrisi:");
        oyun.MatrisiYazdir();

        Console.ReadLine();
    }
}
