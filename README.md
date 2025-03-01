# NAFS2

// 1. For döngüsü ile sayının rakamlarının toplamını bulan algoritma
Console.Write("Bir sayı giriniz: ");
int number = int.Parse(Console.ReadLine());
int sum = 0;
for (; number > 0; number /= 10)
{
    sum += number % 10;
}
Console.WriteLine($"Rakamlar toplamı: {sum}");

// 2. While döngüsü ile belirli şartlara uyan değer alan algoritma
int validNumber;
do
{
    Console.Write("10 ile 100 arasında bir sayı giriniz: ");
    validNumber = int.Parse(Console.ReadLine());
} while (validNumber < 10 || validNumber > 100);
Console.WriteLine($"Geçerli sayı: {validNumber}");

// 3. Foreach döngüsü ile yaş kategorisi belirleyen algoritma
int[] ages = {5, 16, 25, 70};
foreach (int age in ages)
{
    string category = age <= 12 ? "Çocuk" : age <= 19 ? "Genç" : age <= 64 ? "Yetişkin" : "Yaşlı";
    Console.WriteLine($"Yaş: {age}, Kategori: {category}");
}

// 4. Bir dizide tekrar eden elemanları bulan algoritma
int[] numbers = {1, 2, 3, 4, 2, 3, 5};
var duplicates = numbers.GroupBy(x => x).Where(g => g.Count() > 1).Select(g => g.Key);
Console.WriteLine("Tekrar eden elemanlar: " + string.Join(", ", duplicates));

// 5. Bir dizide en uzun ve en kısa kelimeyi bulan algoritma
string[] words = {"masa", "bilgisayar", "kalem", "defter"};
var longest = words.OrderByDescending(w => w.Length).First();
var shortest = words.OrderBy(w => w.Length).First();
Console.WriteLine($"En uzun: {longest}, En kısa: {shortest}");

// 6. Kullanıcının girdiği bir cümleyi diziye kaydedip alfabetik sıralayan algoritma
Console.Write("Bir cümle giriniz: ");
string[] sentenceWords = Console.ReadLine().Split(' ').OrderBy(w => w).ToArray();
Console.WriteLine("Sıralı kelimeler: " + string.Join(", ", sentenceWords));

// 7. String dizisinin boyutunu dinamik olarak genişleten algoritma
List<string> dynamicList = new List<string> {"Elma", "Armut"};
dynamicList.Add("Muz");
Console.WriteLine("Güncellenmiş liste: " + string.Join(", ", dynamicList));

// 8. Kullanıcının girdiği kelimeleri listeye kaydedip tersten yazdıran algoritma
List<string> inputWords = new List<string>();
string input;
do
{
    Console.Write("Kelime giriniz (bitirmek için enter): ");
    input = Console.ReadLine();
    if (!string.IsNullOrWhiteSpace(input)) inputWords.Add(input);
} while (!string.IsNullOrWhiteSpace(input));
inputWords.Reverse();
Console.WriteLine("Tersten sıralı kelimeler: " + string.Join(", ", inputWords));

// 9. Rastgele sayılar alıp listeye ekleyen, ortalamayı ve sıralamayı yapan algoritma
List<int> randomNumbers = new List<int>();
Random rnd = new Random();
for (int i = 0; i < 5; i++) randomNumbers.Add(rnd.Next(1, 101));
Console.WriteLine("Ortalama: " + randomNumbers.Average());
randomNumbers.Sort();
Console.WriteLine("Sıralı sayılar: " + string.Join(", ", randomNumbers));

// 10. Bir sayı listesinde 10’dan küçük olanları silen algoritma
List<int> numList = new List<int> {5, 12, 18, 3, 25};
numList.RemoveAll(n => n < 10);
Console.WriteLine("Filtrelenmiş liste: " + string.Join(", ", numList));

// 11. Öğrenci notlarını 50’nin altına düşmeyecek şekilde güncelleyen algoritma
List<int> grades = new List<int> {45, 60, 30, 80, 50};
for (int i = 0; i < grades.Count; i++)
{
    if (grades[i] < 50) grades[i] = 50;
}
Console.WriteLine("Güncellenmiş notlar: " + string.Join(", ", grades));

{
    if (grades[i] < 50) grades[i] = 50;
}
Console.WriteLine("Güncellenmiş notlar: " + string.Join(", ", grades));
