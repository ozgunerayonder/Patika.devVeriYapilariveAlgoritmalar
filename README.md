# Patika.devVeriYapilariveAlgoritmalar
Patika.dev'in Veri Yapıları ve Algoritmaları dersini bitirme projesidir.
# Insertion Sort Projesi
[22,27,16,2,18,6] -> Insertion Sort
1-Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.
2-Big-O gösterimini yazınız.
3-Time Complexity: Average case: Aradığımız sayının ortada olması,Worst case: Aradığımız sayının sonda olması, Best case: Aradığımız sayının dizinin en başında olması.
4-Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.
5-[7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

# 1- Insertion Sort Aşamaları 
 [22|,27,16,2,18,6]
 [22,27|,16,2,18,6]
 [16,22,27|,2,18,6]
 [2,16,22,27|,18,6]
 [2,16,18,22,27|,6]
 [2,6,16,18,22,27]
 
 # 2- Big O Notation Gösterimi
Worst Case : O(n^2)
Avarage Case : O(n^2)
Best Case : O(n)

# 3- Time Complexity
Best Case : [2,6,16,18,22,27]
Worst Case : [27,22,18,16,6,2]

# 4- 18 Sayısının Case Durumu
Dizi sıralandıktan sonra [2,6,16,18,22,27] halini alır.Bu durumda 18 sayısı ortada olarak sayılabilir.
Bu nedenle avarage case kapsamında yer alır. 

# Merge Sort Projesi
[16,21,11,8,12,22] -> Merge Sort
1-Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
2-Big-O gösterimini yazınız.

# 1- Merge Sort Aşamaları
[16,21,11,8,12,22] ilk önce sayı dizisini ikiye böleriz.
- [16,21,11]     [8,12,22]
Daha sonra böldüğümüz dizileri bir daha ikiye böleriz.
- [16,21]   [11]   [8,12]   [22]
Elde edilen diziler 2 veya daha az eleman sayısına ulaştığı için bölme işlemini durduruz.
Her diziyi kendi içinde sıralarız.
- [16,21]   [11]   [8,12]   [22]
Şimdi ise ikili olarak sıraya uygun bir şekilde diziler birleştirilir.
- [11,16,21]   [8,12,22]
Elde edilen diziler uygun bir şekilde bir kez daha birleştirilir.
- [8,11,12,16,21,22]
Ve dizi sıralı hale gelir.

# 2- Big O Notation Gösterimi
Worst case   : O(n*logn)
Average case : O(n*logn)
Best case    : O(n*logn)

# Binary Search Tree Projesi
[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree aşamalarını yazınız.
Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.
# Binary Search Tree Aşamaları

[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisini soldan okumaya başlıyoruz.
Eğer okuduğumuz sayı bir önceki sayıdan büyükse sayının sağına doğru küçükse soluna doğru kök şeklinde ilerliyoruz.

|     Açıklama    |  |  |  |
|--               |- |- |- |
|**root=7**       |  | 7|  |



**5 sayısı 7'den küçük olduğunda 7'nin soluna ekledik**
|   Açıklama  |     |  |  |
|--           |-    |- |- |
|             |     |  | 7|  
|             |     | /|  | 
|**5 ekledik**|**5**|  |  | 


**1 sayısı 5'ten ve 7'den küçük olduğunda 7 ve 5'in soluna ekledik** 
|     Açıklama  |     |  |  |  |  |
|             --|--   |--|- |- |- |
|               |     |  |  |  | 7|  
|               |     |  |  | /|  | 
|               |     |  | 5|  |  |  
|               |     | /|  |  |  | 
|**1 ekledik**  |**1**|  |  |  |  |

**8 sayısı 7'den büyük olduğunda 7'nin sağına ekledik** 
| Açıklama      |  |  |  |  |  |  |     |
|--             |--|--|- |- |- |- |-    |
|               |  |  |  |  | 7|  |     |  
|               |  |  |  | /|  |\ |     | 
|**8 ekledik**  |  |  | 5|  |  |  |**8**| 
|               |  | /|  |  |  |  |     | 
|               | 1|  |  |  |  |  |     |

**3 sayısı  7'den ve 5'ten küçük  olduğunda 5'in soluna, 1'den büyük olduğunda 1'in sağına ekledik**  
|  Açıklama     |  |  |     |  |  |  |  |
|--             |--|--|-    |- |- |- |- |
|               |  |  |     |  | 7|  |  |  
|               |  |  |     | /|  |\ |  | 
|               |  |  | 5   |  |  |  |8 | 
|               |  | /|     |  |  |  |  | 
|               | 1|  |     |  |  |  |  |
|               |  |\ |     |  |  |  |  |
|**3 ekledik**  |  |  |**3**|  |  |  |  |

**6 sayısı 7'den küçük  olduğunda 7'nin soluna, 5'ten büyük olduğunda 5'in sağına ekledik**  
| Açıklama      |  |  |  |  |     |  |  |
|--             |--|--|- |- |-    |- |- |
|               |  |  |  |  | 7   |  |  |  
|               |  |  |  | /|     |\ |  | 
|               |  |  | 5|  |     |  |8 | 
|               |  | /|  |\ |     |  |  | 
| **6 ekledik** | 1|  |  |  |**6**|  |  |
|               |  |\ |  |  |     |  |  |
|               |  |  | 3|  |     |  |  |

**0 sayısı  7'den, 5'ten ve 1'den küçük  olduğunda 1'in soluna ekledik**  
| Açıklama       |     |  |  |  |  |  |  |  |  |
|--              |--   |--|- |- |- |- |- |- |- |
|                |     |  |  |  |  |  | 7|  |  |  
|                |     |  |  |  |  | /|  |\ |  | 
|                |     |  |  |  | 5|  |  |  |8 | 
|                |     |  |  | /|  |\ |  |  |  |
|                |     |  | 1|  |  |  |6 |  |  |
|                |     | /|  |\ |  |  |  |  |  |
| **0 ekledik**  |**0**|  |  |  | 3|  |  |  |  |

**9 sayısı  7'den ve 8'den büyük olduğunda  8'in sağına ekledik**  
| Açıklama     |  |  |  |  |  |  |  |  |  |  |     |
|--            |--|--|- |- |- |- |- |- |- |- |-    |
|              |  |  |  |  |  |  | 7|  |  |  |     |  
|              |  |  |  |  |  | /|  |\ |  |  |     | 
|              |  |  |  |  | 5|  |  |  |8 |  |     | 
|              |  |  |  | /|  |\ |  |  |  |\ |     | 
| **9 ekledik**|  |  | 1|  |  |  |6 |  |  |  |**9**|
|              |  | /|  |\ |  |  |  |  |  |  |     |
|              | 0|  |  |  | 3|  |  |  |  |  |     |


**4 sayısı  7'den ve 5'ten küçük olduğunda 5'in soluna, 1'den ve 3'ten büyük olduğunda 3'ün sağına ekledik** 
| Açıklama    |  |  |  |  |  |  |     |  |  |  |  |
|--           |--|--|- |- |- |- |-    |- |- |- |- |
|             |  |  |  |  |  |  | 7   |  |  |  |  |  
|             |  |  |  |  |  | /|     |\ |  |  |  | 
|             |  |  |  |  | 5|  |     |  |8 |  |  | 
|             |  |  |  | /|  |\ |     |  |  |\ |  |
|             |  |  | 1|  |  |  |6    |  |  |  | 9|
|             |  | /|  |\ |  |  |     |  |  |  |  |
|             | 0|  |  |  | 3|  |     |  |  |  |  |
|             |  |  |  |  |  |\ |     |  |  |  |  |
|**4 ekledik**|  |  |  |  |  |  |**4**|  |  |  |  |

**2 sayısı  7'den ve 5'ten küçük olduğunda 5'in soluna, 1'den büyük olduğunda 1'in sağına ve 3'ten küçük olduğunda 3'ün soluna ekledik** 
| Açıklama    |  |  |     |  |  |  |  |  |  |  |  |
|--           |--|--|-    |- |- |- |- |- |- |- |- |
|             |  |  |     |  |  |  | 7|  |  |  |  |  
|             |  |  |     |  |  | /|  |\ |  |  |  | 
|             |  |  |     |  | 5|  |  |  |8 |  |  | 
|             |  |  |     | /|  |\ |  |  |  |\ |  | 
|             |  |  | 1   |  |  |  |6 |  |  |  | 9|
|             |  | /|     |\ |  |  |  |  |  |  |  |
|             | 0|  |     |  | 3|  |  |  |  |  |  |
|             |  |  |     | /|  |\ |  |  |  |  |  |
|**2 ekledik**|  |  |**2**|  |  |  |4 |  |  |  |  |
   


