# C64AssemblyCourse2021

Prerequisites
- preferably Windows 10 PC
- GitHub account
- base programming skills

*Miről szól? A Commodore 64 programozásáról assembly nyelven a mai modern PCken. A hardverről és az alap lehetőségekről. Hobbi szinten*

*Miről nem szól? Nem szól a BASICről, a KERNALról (beépített C64 "OS"), sőt a legkifinomultabb "world record" effektekről SEM. :)*

Kérdezni ér! Sőt, kötelező!! :) 

Tematika:

# Lesson 1
- Programozási alapok, ugye mindenki tisztában van? Szekvencia, iteráció, szelekció? :) 
- binary, decimal, hexadecimal :) 

- Cross assembly lehetőségek (szövegszerkesztő, fordítók (assembler, compiler), tömörítők (compressor, "cruncher"), emulátor)
Hogyan lehet felépíteni egy kényelmes fordító környezetet?
1. Szövegszerkesztő (Notepad, Notepad++, VS Code) - fontos, hogy legyen szintaktikai kiemelés, esetleg automatikusan tudja indítani a fordítást valamilyen módon
2. Fordító/Assembler - ebből eléggé sok létezik, de fordítás után ugyanaz a kód keletkezik: a végeredmény mindig C64 assembly :) Mindenkinek más állhat kézre, én a 64TASS-t használom, a példák is ezen fognak rendesen fordulni. Ismert és használt assemblerek, egy nemrég készített felmérés: https://fragab.de/35Ff8TS
3. Tömörítők (command line tool-ok): pl. ByteBoozer2, Exomizer, stb
4. Emulator: egyértelműen a VICE (https://vice-emu.sourceforge.io)

- A vas /  hardware
Miből áll a C64? :)
CPU, SID, VIC-II, CIA (I/O), memória

- A memória - memory map/layout
https://www.c64-wiki.com/wiki/Memory_Map
http://sta.c64.org/cbm64mem.html 

64k RAM - 65536 byte tárolása ($0000 - $FFFF). 
+ 4k BASIC ROM ($A000 - $BFFFF)
+ 4k KERNAL ROM ($E000 - $FFFF)
+ 2x2k Character ROM
+ I/O area
+ ScreenRAM és ColorRAM
+ Zero Page, lapozás megértése
+ Fix, mozdíthatatlan memóriahelyek: $01, $0100-$01FF, IRQ vektorok ($fffa-$fffb(NMI) $fffe-$ffff (IRQ))

- 6502/6510 processzor, regiszterek, képességek (összeadás, kivonás, összehasonlítás, BCD (neeem))
http://www.6502.org/tutorials/6502opcodes.html
+ Utasítások (mnemonics), illegal opcodes (??)
+ bit műveletek, AND / OR
+ Címzési módok
+ Processzor státus flag-ek, A X Y regiszterek
+ Program Counter (PC), Stack Counter (SC)
+ Execution time: cycle
+ Verem (Stack) - LIFO (https://www.c64-wiki.com/wiki/Stack)

- VIC-II (a videóprocesszor)
+ Képernyő felépítése, méretei
+ Karakteres és grafikus üzemmódok / Multicolor vs. Hires (https://codebase64.org/doku.php?id=base:built_in_screen_modes)
+ 16 szín (https://www.c64-wiki.com/wiki/Color)
+ A busz megosztása a CPU és a VIC között
+ csak 16k RAM-ot lát a VIC! Bank Switching/bankváltás
+ A $d800 az mindig $d800 ! :) 
+ sprite-ok, sprite pointerek

- SID
+ erről csak nagyon röviden. Music player rutinok

- IRQ, megszakítások (VIC IRQ, NMI, stb)
+ egy vicces, jó leírás :) https://dustlayer.com/c64-coding-tutorials/2013/4/8/episode-2-3-did-i-interrupt-you

TUTORIALS
+ Hello world
+ Border villogtatás
+ IRQ zenelejátszás
+ sprite mozgatás? Szinusszal?
+ Raszter effektek
+ Scroller
+ Grafika megjelenítése

RESOURCES
Nagyon hasznos oldalak:
https://codebase64.org/ Bármi, ami C64 programozás, az egyik (ha nem) a legjobb ilyen oldal

