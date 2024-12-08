Idee:

- Stellen topologische Sortierungen fuer gewisse Ordnungsrelationen auf einer Menge/Liste von Objekten her

Selection Sort

# Vorgehen:

- Sortierte Partition am Anfang der Liste
- Finde kleinste Zahl in unsortierter Partition, setze an naechsten Index der sortierten Partition

# Example:

![Min-index 25 12 22 Smallest element: 11 11 Swapping Elements Min—index 11 25 Smallest element: 12 12 22 64 Swapping Elements Min—index Smallest element: 22 11 11 11 12 12 12 25 22 Swapping Elements Min_index 22 Smallest element: 25 swa p ped with itself Min_index Srnallest elernent= 64 22 25 swa p ped with itself ](Exported%20image%2020241208232748-0.png)  

# Code:

![Input: Array A der Länge n, partielle Ordnung Output: A topologisch sortiert for i 4— O to n —2 do: Python code selectionsort . py selectionSort (A): def # Sort the given list A n = len(A) for range (O ,n-l): a for j 4— i + 1 to n — 1 do: if AL j] -K A[i] then swap(A [i] , A Lj]) range (1+1 , n): for j if input ( ) . split ( ) selectionSort (A) print ](Exported%20image%2020241208232749-1.png)

# Eigenschaften:

Selection Sort funktioniert fuer arbitraere **partielle** Ordnungen!  
Selection Sort hat Laufzeit O(n^2)  
Selection sort ist stabil  
Selection sort ist in situ  
Insertion Sort

# Vorgehen:

- Baut sortierte Teilliste zu Beginn auf
- Dabei naechstes Element an richtige Stelle der Teilliste gesetzt

# Example:

![First Pass 
Second Pass 
Third Pass 
Forth Pass 
Fifth Pass 
Insertion Sort ](https://graph.microsoft.com/v1.0/users('damian.grunert@gmx.de')/onenote/resources/0-e96c1fa0ee504a4da6759c515294e6d2!1-37C7E9FCFE583605!s4088cd6f62334569abc1e4890a213981/$value)

# Code:

![Input: Array A der Länge n, totale Ordnung Output: A sortiert fori K— 1 to n — 1 do while k > 0 A s K 1] do A Ck] ACk-1] Python code insertionsort . py insertionSort (A): def len(A) n range (1, n): for i in s k i while and k 1 s input ( ) . split ( ) insertionSort (A) print ](Exported%20image%2020241208232750-3.png)

# Eigenschaften:

Insertion sort funktioniert fuer arbitraere **totale** Ordnungen!  
Insertion sort hat Laufzeit O(n^2)  
Insertion sort ist stabil  
Insertion sort ist in situ  
Merge Sort:

# Vorgehen:

- Liste in gleichgrosse Teillisten aufspalten
- Nach Reissverschlussprinzip beide Listen mergen

# Example:

![Exported image](Exported%20image%2020241208232754-4.png)

# Code:

![](https://graph.microsoft.com/v1.0/users('damian.grunert@gmx.de')/onenote/resources/0-8794321f35104781b19baa39bd4cae50!1-37C7E9FCFE583605!s4088cd6f62334569abc1e4890a213981/$value) ![Exported image](Exported%20image%2020241208232825-6.png) ![Exported image](Exported%20image%2020241208232826-7.png)

# Eigenschaften:

Merge-Sort funktioniert auf beliebigen totalen Ordnungen  
Merge-Sort hat Laufzeit O(n log(n)), da 2log(n) Rekursionsschritten mit jeweils max n Operationen  
Merge sort ist stabil  
Merge sort ist nicht in situ  
Quick Sort:

# Idee:

- Teile Liste in Partition <= Pivot, Pivot, Partition > Pivot auf
- Setze entsprechend zusammen

# Example:
   

# Code:

![Exported image](Exported%20image%2020241208232827-8.png) ![Exported image](Exported%20image%2020241208232829-9.png)

# Eigenschaften:

Quicksort funktioniert auf total sortierten Mengen  
Quicksort hat I.A. Laufzeit in O(n^2). Wird als Pivot-Element der Median gewaehlt, so hat es Laufzeit in O(n log(n))  
Quicksort ist nicht stabil  
Quicksort ist in place