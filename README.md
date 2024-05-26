# SI_2024_lab2_223043
Vase Lazarev 223043


2. 

![223043.drawio.png](pics%2F223043.drawio.png)

3. Ciklomatskata kompleksnost na dadeniot kod e 10, go presmetav spored formulata P+1.
Brojot na predikatni jazli, t.e. P iznesuva 9, so sto dobivame 10 (9+1), a istoto moze da se sogleda i so brojot na regioni od grafikot.


4. Test cases for every branch

![branches.PNG](pics%2Fbranches.PNG)

1) dokolku allItems = null => frla RuntimeException("allItems list can't be null!");
2) dokolku imame 2 items, pr. Item("", "033", 500, .15) i Item("laptop","333",700,0) i payment=1500, togas ke gi izmineme najgolemiot del od branchovite i ke vrati true bidejki sumata e pomala od paymentot;
3) dokolku imame 1 Item("door", "", 1500, .5) i paymentot = 1500, togas ke frli runtime exception ("No barcode!"), bidejki vo branch 9 uslovot nema da bide ispolnet i odi vo elsot, t.e. preminuva na branch 19 kade go frla toj exception i odi na krajot odnosno branch 25;
4) dokolku imame 1 item, ("bed", "333", 2000, .5) i paymentot = 1500, togas ke vrati false bidejki celata suma ke bide pomala od paymentot;
5) dokolku imame 1 Item("barcodeScanner", "01BC", 500, 0) i paymentot = 500, togas ke frli runtime exception ("Invalid character in item barcode!"), bidejki nema da se sovpaga so karakter od allowed barcode poradi vnesenite bukvi vo barcode, odnosno vo 3toto izminuvanje na vnatresniot for ciklus, vo if uslovot, od branch 14 odi vo branch 15 i tamu go frla isklucokot i odi na posledniot branch 25 za kraj na programata

5. Multiple Condition test cases

if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0').

1) Item("laptop", "033", 500, .15) -> true + true + true = true;
2) Item("laptop", "333", 300, .15) -> false + true(nebitno) + false(nebitno) = false; dokolku prvoto e false ke dobieme vo sekoj slucaj false, 2 i 3 ne se bitni sto ke bidat;
3) Item("laptop", "333", 500, .15) -> true + true + false = false;
4) Item("laptop", "333", 500, 0) -> true + false + true (nebitno) = false;


