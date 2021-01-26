# C64AssemblyCourse2021

Prerequisites
- preferably Windows 10 PC
- GitHub account
- base programming skills
- hexadecimal counting :) 

*Miről szól? A Commodore 64 programozásáról assembly nyelven a mai modern PCken. A harderről és az alap lehetőségekről. Hobbi szinten*

*Miről nem szól? Nem szól a BASICről, a KERNALról (beépített C64 "OS"), sőt a legkifinomultabb "world record" effektekről SEM. :)*

Kérdezni ér! Sőt, kötelező!! :) 

Tematika:

# Lesson 1
- Programozási alapok, ugye mindenki tisztában van? Szekvencia, iteráció, szelekció? :) 

- Cross assembly lehetőségek (szövegszerkesztő, fordítók (assembler, compiler), tömörítők (compressor, "cruncher"), emulátor
Hogyan lehet felépíteni egy kényelmes fordító környezetet?

- C64 hardware
Miből áll a C64? :)
CPU, SID, VIC-II, CIA (I/O), memória

- memory map/layout
64k RAM
+ 4k BASIC ROM
+ 4k KERNAL ROM
+ 2x2k Character ROM
+ I/O area
+ ScreenRAM és ColorRAM
+ Zero Page, lapozás megértése
+ Fix, mozgathatatlan memóriahelyek: $01, $0100-$01FF, IRQ vektorok ($fffa-$fffb(NMI) $fffe-$ffff (IRQ))

https://www.c64-wiki.com/wiki/Memory_Map
http://sta.c64.org/cbm64mem.html 


- 6510 processzor, regiszterek, képességek (összeadás, kivonás, összehasonlítás, BCD (neeem), 
- Mnemonikok

- VIC-II (a videóprocesszor)
+ busz megosztás a CPUval
+ csak 16k RAM-ot lát a VIC! Bank Switching/bankváltás
+ A $d800 az mindig $d800 ! :) 

- IRQ, megszakítások (VIC IRQ, NMI, stb)
