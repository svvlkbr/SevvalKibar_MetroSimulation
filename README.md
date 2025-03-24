'''markdown
   Sürücüsüz Metro Simülasyonu

Bu proje, Python kullanılarak geliştirilen sürücüsüzmetro sistemi simülasyonudur.Amaç, bir metro aracının duraklar arasında en verimli ve güvenli şekilde hareket etmesini sağlamaktır.Güzergah belirlemede akıllı algoritmalar kullanılmıştır.


   Kullanılan Teknolojiler ve Kütüphaneler
-Python 3
-heapq:A* algoritmasında öncelik sırası oluşturmak için kullanıldı (min-heap yapısı).
-collections.deque:BFS algoritmasında kuyruk veri yapısı için kullanıldı.
-time:Simülasyonlarda gecikme efekti vermek için kullanılabilir.


   Algoritmaların Çalışma Mantığı
 BFS (Breadht-First Search)
-Genişlik öncelikli arama algoritmasıdır
-Metro ağı üzerinde en kısa yolu bulmak için kullanıldı.
-Her durağı sırasıyla kontrol eder, en kısa yol garantilidir.
-Kuyruk (queqe) yapısı kullanılır: İlk giren ilk çıkan mantığı (FIFO).


 A* (A STAR) Algoritması
-Daha akıllı bir arama algoritmasıdır.
-BFS gibi çalışır ama heuristic (tahmin) kullanılır,yani hedefe yakın düğümleri önce dener.
heapq ile öncelikli kuyruk yapılır, her durağın skoru hesaplanır:
  f(n)=g(n)+h(n)
   -g(n)= şu ana kadarki yol maliyeti
   -h(n)= hedefe olan tahmini uzaklık


   Neden Bu Algoritmalar
-BFS, küçük haritalarda garantili ve hızlı sonuç verir.
-A*, daha büyük ve karmaşık haritalarda daha verimli çalışır çünkü hedefe daha kısa sürede ulaşabilir.


  Örnek Kullanım ve Test Sonuçları
 Kullanım
bash
python sevvalkibar_metro_simulation.py

