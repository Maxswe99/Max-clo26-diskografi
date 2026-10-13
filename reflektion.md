# Reflektion — Inlämning 1

**Namn:** Max Svensson 
**Datum:** 2026-10-13

---

## Vad var svårast?

definitivt VG delen med many-to-many\
veta vad jag ville ha för kolumner i mina tabeller

## Förklaringar
vi har many-to-many för att kunna slå ihop nycklar till en unik nyckel för att kunna separera vem som gör vad i en låt.\
den länkar till både artist och låt id. den hindrar också att det blir dubbletter av samma artist eller låt. en artist kan ha flera låtar eller tvärtom

join är att systemet kan hämta information från flera tabeller som är sammanslagna med join commandot. utan det så vet inte systemet vilken information man letar efter

min tabellstruktur har i åtanke med normalisering och redundans. behöver inte upprepa utan kan ändra enskilda rader för ändringar

---

## Vad lärde du dig?

1. Att varchar sparar utrymme (dynamiskt) istället för char som tar fast minne. så varchar(100) sätter en gräns på 100 tecken\
men använder bara 3 om det skulle stå "Hej". Detta lärde jag mig genom att string inte är ett korrekt format
2. Values skrivs bara en gång som alla nyckelord. Skrev först VALUES album1 sen VALUES album2 vilket inte var rätt.
3. Att "AS" i tex. Från Query 3, SELECT album_id, COUNT(song_name) AS total_songs. Döper om titeln från COUNT(song_name) till total_songs för renlighet
4. (DMBL) Sammansatt primärnyckel (Composite Primary Key) flera nycklar slås ihop och blir en unik nyckel
5. hur man lägger till bilder
6. att DESC inte finns i GROUP BY utan ORDER BY
7. LIMIT

---

## Hur använde du SQL i praktiken — vad kändes naturligt och vad var förvirrande?

det som kändes naturligt var att jag näst in till visste exakt vad jag ville skriva för att få ut rätt information till\
alla querys som var listade i inlämningen. SQLZoo var till stor nytta.

det som var mest förvirrande och huvudvärk var hela many-to-many delen och att ibland så skrev jag fel i https://sqliteonline.com/
där jag skapade en temporär databas för att säkerhetställa att mina kommandon gjorde det dem skulle.

---

## Om du hade mer tid — vad hade du lagt till eller gjort annorlunda?

tycker att jag har gjort det jag kan... och gjorde min tabell utan att tänka på normalisering från början.
