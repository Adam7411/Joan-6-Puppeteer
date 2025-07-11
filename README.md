# Joan-6-Puppeteer

Na urządzeniu Joan 6 można wyświetlić obraz dashboardu Home Assistant używając niestandardowego dodatku **Puppeteer**.  
Dodatek działa jako serwer HTTP, który generuje zrzuty ekranu (screenshots) z interfejsu Home Assistant.  

> ❗ Uwaga: Puppeteer umożliwia **tylko podgląd** – nie obsługuje dotykowych przycisków ani interakcji.



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

Teraz według dokumentacji wklej link w przeglądarke 
    ```bash
    http://adresHA:10000/lovelace/0?viewport=1000x1000
    ```
