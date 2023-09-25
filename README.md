# Calisma
Array.Resize&amp;Array.Sort&amp;foreach_EXAMPLE


int[] sayilar = new int[0];

int ciftsayac = 0 , teksayac = 0;
double tektoplam = 0 , cifttoplam = 0, tekortalama = 0 , ciftortalama = 0 ;

Console.Write("Lütfen Kaç Adet Sayı Girileceğini Belirtiniz : ");
int n = Convert.ToInt32(Console.ReadLine());

for (int i = 0; i < n ; i++)
{
     Console.Write("Lütfen Bir Sayı Giriniz : ");
     int sayi = Convert.ToInt32(Console.ReadLine());
     Array.Resize(ref sayilar, sayilar.Length + 1);
	 sayilar[i] = sayi;
}
Console.WriteLine("Sıralamadan Önceki Hali");
foreach (int sayi in sayilar)
{
    Console.WriteLine(sayi);
}
Array.Sort(sayilar);
Console.WriteLine("Sıralamadan Sonraki Hali");
foreach (int sayi in sayilar)
{
    Console.WriteLine(sayi);
}
Console.WriteLine("=================================");
foreach (int sayi in sayilar)
{
    if (sayi % 2 == 0)
    {
        cifttoplam = cifttoplam + sayi;
        ciftsayac++;
    }
    else if (sayi % 2 == 1)
    {
        tektoplam = tektoplam + sayi;
        teksayac++;
    }
}

ciftortalama = cifttoplam / ciftsayac;
tekortalama = tektoplam / teksayac;

Console.WriteLine($"Yazılan Tek Sayıların Adeti : {teksayac} \nYazılan Çift Sayıların Adeti : {ciftsayac}");
Console.WriteLine("=================================");
Console.WriteLine($"Yazılan Tek Sayıların Toplamı : {tektoplam} \nYazılan Cıft Sayıların Toplamı :{cifttoplam}");
Console.WriteLine("=================================");
Console.WriteLine($"Yazılan Tek Sayıların Ortalaması : {tekortalama} \nYazılan Cıft Sayıların Ortalaması : {ciftortalama}");
Console.WriteLine("=================================");


