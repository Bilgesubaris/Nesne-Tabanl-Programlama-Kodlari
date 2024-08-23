using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System;


namespace ConsoleApp5
{
    class Sekiller
    {
        public int uzunluk1;
        public int uzunluk2;
    }

    class Dikdortgen : Sekiller
    {
        public void Ciz(bool dolu)
        {
            for (int i = 0; i < uzunluk1; i++)
            {
                for (int j = 0; j < uzunluk2; j++)
                {
                    if (dolu)
                    {
                        Console.Write("*");
                    }
                    else
                    {
                        if (i == 0 || i == uzunluk1 - 1 || j == 0 || j == uzunluk2 - 1)
                        {
                            Console.Write("*");
                        }
                        else
                        {
                            Console.Write(' ');
                        }
                    }
                }
                Console.WriteLine();
            }
        }
    }

    class EskenarUcgen : Sekiller
    {
        public void Ciz(bool dolu)
        {
            for (int i = 0; i < uzunluk1; i++)
            {
                for (int j = 0; j <= i; j++)
                {
                    if (dolu)
                    {
                        Console.Write("*");
                    }
                    else
                    {
                        if (i == uzunluk1 - 1 || j == 0 || j == i)
                        {
                            Console.Write("*");
                        }
                        else
                        {
                            Console.Write(' ');
                        }
                    }
                }
                Console.WriteLine();
            }
        }
    }

    class EskenarDortgen : Sekiller
    {
        public void Ciz(bool dolu)
        {
            for (int i = 0; i < uzunluk1; i++)
            {
                for (int j = 0; j < uzunluk2; j++)
                {
                    if (dolu)
                    {
                        Console.Write("*");
                    }
                    else
                    {
                        if (i == uzunluk1 - 1 || j == 0 || j == uzunluk2 - 1)
                        {
                            Console.Write("*");
                        }
                        else
                        {
                            Console.Write(' ');
                        }
                    }
                }
                Console.WriteLine();
            }
           
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
         

            Console.WriteLine("1. Dikdörtgen\n2. Eşkenar Üçgen\n3. Eşkenar Dörtgen");
            Console.Write("Lütfen çizmek istediğiniz şeklin numarasını giriniz: ");
            int secim = Convert.ToInt32(Console.ReadLine());

            Console.Write("Dolu mu (1) - Boş mu (0): ");
            bool doluSecim = Convert.ToInt32(Console.ReadLine()) == 1;

            switch (secim)
            {
                case 1:
                    Console.Write("Dikdörtgen Uzunluğu 1 giriniz: ");
                    int dikUzunluk1 = Convert.ToInt32(Console.ReadLine());

                    Console.Write("Dikdörtgen Uzunluğu 2 giriniz: ");
                    int dikUzunluk2 = Convert.ToInt32(Console.ReadLine());
                    Dikdortgen dikdortgen = new Dikdortgen();
                    dikdortgen.uzunluk1 = dikUzunluk1;
                    dikdortgen.uzunluk2 = dikUzunluk2;
                    dikdortgen.Ciz(doluSecim);
                    break;

                case 2:
                    Console.Write("Eşkenar Üçgen Uzunluğu giriniz: ");
                    int ucgenUzunluk1 = Convert.ToInt32(Console.ReadLine());
                    EskenarUcgen eskenarUcgen = new EskenarUcgen();
                    eskenarUcgen.uzunluk1 = ucgenUzunluk1;
                    eskenarUcgen.Ciz(doluSecim);
                    break;

                case 3:
                    Console.Write("Eşkenar Dörtgen İlk Uzunluğu  giriniz: ");
                    int dortgenUzunluk1 = Convert.ToInt32(Console.ReadLine());
                    
                    Console.Write("Eşkenar Dörtgen İkinci Uzunluğu  giriniz: ");
                    int dortgenUzunluk2 = Convert.ToInt32(Console.ReadLine());

                    EskenarDortgen eskenarDortgen = new EskenarDortgen();
                    eskenarDortgen.uzunluk1 = dortgenUzunluk1;
                    eskenarDortgen.uzunluk2 = dortgenUzunluk2;
                    Console.WriteLine("Eskenar dörtgen");
                    eskenarDortgen.Ciz(doluSecim);
                    break;

                default:
                    Console.WriteLine("Geçersiz seçim.");
                    break;
            }

            Console.Read();
        }
    }
}
