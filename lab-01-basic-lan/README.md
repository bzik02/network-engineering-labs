# LAB 01 - Basic LAN
## 1. Opis projekta 
Cilj ovoga projekta je bio povezati tri računala od tri zaposlenika u zamišljenoj IT tvrtki tako da su računala u lokalnoj mreži. Projekt je rađen u Cisco Packet Tracer.
## 2. Mrežna topologija
Zadano mi je bilo imena uređaja: PC-ADMIN, PC-SALES, PC-MANAGER njihova IP adresa: PC-ADMIN: 192.168.10.10, PC-SALES: 192.168.10.20, PC-MANAGER: 192.168.10.30 i Subnet maska: 255.255.255.0. Prvo sam stavio središnji uređaj (Switch) iz njega sam provukao bakreni mrežni kabel i spojio ga na PC-ADMIN, nakon toga sam isto tako napravio za PC-SALES i PC-MANAGER to zovemo "zvjezdasta topologija" jer su sva tri računala pojedinačno povezana na središnji switch. 
## 3. IP konfiguracija
Kao što sam naveo u "Mrežnoj topologiji" zadane su mi bile IP adrese i Subnet mask (PC-ADMIN: 192.168.10.10, PC-SALES: 192.168.10.20, PC-MANAGER: 192.168.10.30 i Subnet maska: 255.255.255.0). Zašto svako računalo ima različitu IP adresu to možemo objasniti kao npr. kako ljudi imaju svoja imena tako i računala da bi komunicirala moraju imati neka imena za komunicirati, a zašto je subnet maska bila jednaka za svako računalo u ovome mojemu slučaju jer maska pomaže računalu odrediti koji dio IP adrese označava mrežu a koji uređaj. Nismo trebali Default Gateway jer smo imali tri računala koja su morala međusobno komunicirati i nismo imali router.
## 4. Testiranje komunikacije
Komunikaciju sam testirao tako da sam na svakom od računala upalio Command Prompt na računalu(PC-ADMIN) upisao sam ping IP adresa od računala(PC-SALES) "ping 192.168.10.20", onda sam na računalu(PC-SALES) pingao IP adresu od računala(PC-MANAGER)
"ping 192.168.10.30" i na kraju sam s računalo(PC-MANAGER) pingao računalo(PC-ADMIN) "ping 192.168.10.10". Znao sam da komuniciraju tako što sam dobio povratnu informaciju "Reply from 192.168.10.10 bytes=32 time=5 TTL=128".
## 5. Rješavanje problema
Odlučio sam na računalu(PC-SALES) promijeniti IP adresu u 192.168.11.20, nakon što sam to bio napravio bio sam pingao računalo(PC-SALES) i izbacilo mi je Request timed out. Promjenom IP adrese uz istu subnet masku računalo(PC-SALES) je prešlo u drugu podmrežu a pošto nismo imali router, komunikacija nije mogla normalno funkcionirati. Ponovno sam bio vratio zadanu IP adresu i pingao opet računalo(PC-SALES) i dobio sam "Reply" nazad.
## 6. Što sam naučio
Danas sam naučio ne pretpostavljati odmah uzrok, nego sustavno provjeriti moguće probleme. Naučio sam isto tako da računala u istoj mreži mogu komunicirati preko switcha bez routera.
