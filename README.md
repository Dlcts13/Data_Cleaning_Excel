# Data_Cleaning_Excel
---------------------------------------
Scop
---------------------------------------

Acest fișier descrie pașii urmați pentru curățarea și pregătirea setului de date înainte de analiză.
Obiectivul a fost să obținem un fișier coerent, complet și ușor de analizat, fără erori de formatare sau inconsistențe.

---------------------------------------
1. Verificarea structurii inițiale
---------------------------------------

---------------------------------------
2. Curățarea pe coloane
---------------------------------------
Order ID
*Verificat că nu există valori lipsă sau duplicate.
*Coloana a fost păstrată nemodificată, deoarece reprezintă identificator unic al comenzii.

Customer Name
*Golurile au fost completate cu eticheta Unknown Customer.
*Au fost eliminate spațiile suplimentare și caracterele invizibile folosind =TRIM() și =CLEAN().
*Numele au fost uniformizate în format „Prenume Nume” cu =PROPER().

Order Date
*Formatele diferite (de tip 2025-03-08 și 03/07/2025) au fost standardizate.
*Coloana a fost convertită în format de dată reală folosind Data → Text to Columns → Date (DMY).

Ship Date
*Verificate valorile lipsă și consistența cu Order Date.
*Confirmat că toate valorile sunt în format de dată.
*Opțional, s-a calculat timpul de livrare (Ship Date - Order Date) pentru verificare logică.

Product
*Verificat ca toate valorile să fie text, fără spații inutile sau caractere neobișnuite.
*Denumirile de produse au fost uniformizate (ex: „laptop” → „Laptop”).

Quantity
*Convertită la format numeric.
*Eliminat textul și caracterele non-numerice.
*Verificate valorile negative sau neobișnuite.
*Erorile identificate au fost corectate manual.

Price
*Eliminat simbolul $ sau alte caractere non-numerice.
*Convertită la format numeric.
*Uniformizat numărul de zecimale.

Total Price
*Verificat că este numeric și corespunde cu Quantity * Price.
*Valorile incoerente au fost recalculat sau corectate manual.

Region
*Uniformizate valorile (ex: „north” → „North”).

-----------------------------------------------------------
3. Curățarea generală
-----------------------------------------------------------
Eliminat rândurile complet goale.
Verificate duplicatele la nivel de rând complet.
Denumirile coloanelor au fost standardizate (fără spații inutile).
Toate valorile numerice au fost formatate coerent (număr, fără text).
Toate datele au fost salvate într-un format compatibil (.xlsx).

-----------------------------------------------------------
4. Rezultat final
-----------------------------------------------------------
Setul de date rezultat este:
Fără valori lipsă esențiale.
Cu formate de date, text și numere coerente.

Pregătit pentru analiză, raportare și vizualizare ulterioară.
