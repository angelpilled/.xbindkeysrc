# xbindkeysrc konfig

[English notes] This repository was meant for hungarian keyboard layouts on Thinkpad X260 laptops running xbindkeys on Linux (might work on other models as well).

Sziasztok! Ez a repo magyar Thinkpad X260 billentyűzetekre készült. Más Thinkpadokon nem tudtam tesztelni, de lehet, hogy működnek rajta is.

Szükséges csomag nyilván az **xbindkeys**.
A konfigurációs fájl a helyes telepítés után (.xbindkeysrc) a home (~/.xbindkeysrc) könyvtárban lesz elérhető.

A repo-t nem muszáj leklónozni/letölteni, a kódot ki is lehet másolni!

## Szükséges csomagok
+ xbindkeys
+ xdotool

A szöveg, amit a konfig fájlban hozzáadtam:

```
# Benagyítás (Win+ó)
"sleep 0.1 && xdotool key Control_L+KP_Add"
Mod4 + oacute

# Kinagyítás (Win+ü)
"sleep 0.1 && xdotool key Control_L+KP_Subtract"
Mod4 + udiaeresis

# Csillag írása (Win+BalAlt+ö)
"sleep 0.1 && xdotool key KP_Multiply"
Mod4 + Alt + odiaeresis

# Plusz írása (Win+BalAlt+ó)
"sleep 0.1 && xdotool key KP_Add"
Mod4 + Alt + oacute

# Minusz írása (Win+BalAlt+ü)
"sleep 0.1 && xdotool key KP_Subtract"
Mod4 + Alt + udiaeresis
```

Miután az **.xbindkeysrc** fájlt módosítva lett, újra kell indítanod (ha még be futtatva volt)!
Kikapcsolni a `killall -HUP xbindkeys` paranccsal kell, utána elindítod újra.

Ugyanez a forráskód elérhető a fenti fájlban is.

Használt források:
+ https://www.oreilly.com/library/view/xlib-reference-manual/9780937175262/16_appendix-h.html
+ showkey
+ xbindkeys --multikeys
