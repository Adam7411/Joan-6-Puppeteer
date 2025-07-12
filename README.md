# Joan-6-Puppeteer

Na urządzeniu Joan 6 można wyświetlić obraz dashboardu Home Assistant używając niestandardowego dodatku **Puppeteer**.  
Dodatek działa jako serwer HTTP, który generuje zrzuty ekranu (screenshots) z interfejsu Home Assistant.  

> ❗ Uwaga: Puppeteer umożliwia **tylko podgląd** – nie obsługuje dotykowych przycisków ani interakcji. Jest to ogromny minus ale może się komuś przyda tylko do podglądu temperatur czy też wykresów.

<img width="553" height="570" alt="jak na tabytułu" src="https://github.com/user-attachments/assets/e38bb6be-86b4-492f-a1b7-013b5965703d" />



## 📥 Instalacja dodatku

1. Dodatek pobieramy z https://github.com/balloob/home-assistant-addons/blob/main/puppet/README.md
   <img width="1886" height="845" alt="1t" src="https://github.com/user-attachments/assets/df7b0b49-222c-4018-acd2-04b3a4adb362" />

2. Dodaj to repozytorium
3. Zainstaluj

Aby dodatek mógł uzyskać dostęp do Twojego interfejsu HA:

1. Wejdz w profile zakłądka Bezpieczeństwo.
2. Przewiń do sekcji **TWÓRZ TOKEN**.
3. Kliknij **Utwórz token** i nadaj mu nazwę, np. `puppeteer`.
   ![3](https://github.com/user-attachments/assets/4ad81063-ed29-46df-ba44-404fd06ae419)

4. Skopiuj wygenerowany token.


## ⚙️ Konfiguracja dodatku

1. Otwórz konfiguracje dodatku `puppet`.
2. Wklej swój **long-lived token** do pola `token`.
3. Zapisz ustawienia i **uruchom** dodatek.
   <img width="1441" height="695" alt="2t" src="https://github.com/user-attachments/assets/665bcba9-b23c-49d9-a99b-dc31560f0c0b" />

4. Po starcie uruchamia się serwer HTTP na porcie 10000.

5. Teraz według dokumentacji wklej link w przeglądarke zobaczysz strone z HA 
    ```
    http://TWÓJadresHA:10000/lovelace/0?viewport=1000x1000
    ```
6.  Skopiuj ten adres URL ze swoim adresem HA
7.  Wróć do panelu **Visionect Software Suite**, przejdź do ustawień swojego tabletu  
    <img width="1634" height="701" alt="Bez tytułu" src="https://github.com/user-attachments/assets/9f5f3654-e330-4979-b16a-4193b0567983" />

8. W polu **Display web page** wklej skopiowany adres dashboardu. Zapisz zmiany.
      <img width="660" height="649" alt="image" src="https://github.com/user-attachments/assets/f1f99062-648f-423b-a6f2-a8c43ed8faad" />
9. Po chwili na ekranie tabletu powinien pojawić się twój dashboard z Home Assistant. ustaw odświeżanie  Enable automatic content refresh  np. na 40 sekund aby co 40 sekund odświerzało wyświetlaną zawartość.

 inne przykłady
  ```
  http://adresHA:10000/calendar/0?viewport=800x1000
  ```

<img width="556" height="706" alt="image" src="https://github.com/user-attachments/assets/723693a6-b6f6-4588-b969-d10067fdbd75" />


Szybkie wyjaśnienie
<img width="1288" height="801" alt="image" src="https://github.com/user-attachments/assets/03db48fa-1cc1-40e5-a782-bb8ecf2af6a2" />



  ```
  http://adresHA:10000/lovelace/joan/0?viewport=800x1000)
  ```

<img width="553" height="570" alt="jak na tabytułu" src="https://github.com/user-attachments/assets/e38bb6be-86b4-492f-a1b7-013b5965703d" />

   Przykład czarno biały 
   
    http://adresHA:10000/lovelace/joan?viewport=758x1024&eink=2&format=png&wait=3000 



<img width="758" height="1024" alt="image" src="https://github.com/user-attachments/assets/4b702780-bd7f-4573-9658-05d21beb446f" />

Reszta w dokumentacji https://github.com/balloob/home-assistant-addons/blob/main/puppet/README.md

