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
1. Szövegszerkesztő (Notepad, Notepad++, VS Code) - fontos, hogy legyen szintaktikai kiemelés, esetleg automatikusan tudja indítani a fordítást valamilyen módon
2. Fordító/Assembler - ebből eléggé sok létezik, de fordítás után ugyanaz a kód keletkezik: a végeredmény mindig C64 assembly :) Mindenkinek más állhat kézre, én a 64TASS-t használom, a példák is ezen fognak rendesen fordulni. Ismert és használt assemblerek, egy nemrég készített felmérés: https://fragab.de/35Ff8TS
3. Tömörítők (command line tool-ok): pl. ByteBoozer2, Exomizer, stb
4. Emulator: egyértelműen a VICE (https://vice-emu.sourceforge.io)


- C64 hardware
Miből áll a C64? :)
CPU, SID, VIC-II, CIA (I/O), memória

- memory map/layout
64k RAM - 65536 byte tárolása ($0000 - $FFFF). 
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
- Mnemonikok, címzési módok, illegal opcodes (??)

- VIC-II (a videóprocesszor)
+ busz megosztás a CPUval
+ csak 16k RAM-ot lát a VIC! Bank Switching/bankváltás
+ A $d800 az mindig $d800 ! :) 
+ karakteres és grafikus üzemmódok
+ sprite-ok, sprite pointerek
+ kép megjelenítése példa

- IRQ, megszakítások (VIC IRQ, NMI, stb)

+ raszter effektek
+ scroller
