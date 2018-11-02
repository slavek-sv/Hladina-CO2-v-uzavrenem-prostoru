# Hlídání hladiny CO2 v uzavřeném prostoru

Detekce množství CO2 v daném prostoru a následná vizuální signalizace je provedena pomocí stavebnice BigClown od společnosti Hardwario s.r.o. <br>
V tomto projektu je potřeba využít tyto díly: <br>
<ul>Radio Dongle </ul>
<ul>CO2 Monitor Kit</ul>
<ul>Power Controller Kit</ul>
<ul>LED Strip RGBW 1m 144 LED</ul>
<ul>a hlavně Raspberry Pi, doporučuji rovnou koupit "Raspberry Pi 3 Model B" nebo "Raspberry Pi 3 Model B+"</ul>
  
Dále je možné na relé, které je součástí Power Controller Kit-u připojit akustickou signalizaci nebo ovládat zobrazení varování před vstupem do nebezpečného prostru
<br>
Na webové stránce https://www.bigclown.com/cs/ najdete vše jak nainstalovat upravený operační systém pro Raspberry Pi, jak nainstalovat Node-red
<br>
<h2>Jak vše přivést k životu</h2>
<ol>
	<li>Raspberry Pi je plně funkční a na IP adrese Raspberry Pi, port 1880 (příklad IP adresy 10.0.0.20:1880) se zobrazí základní stránky NODE-Red </li>
	<li>Do NODE-red doinstalujeme knihovnu "dashboard"</li>
	<li>dále nakopírujeme obsah souboru "NODE-Red_zakl.verze" do NODE-Red</li>
	<li>Nyní je potřeba provést párování CO2 Monitor Kit a Power Controller Kit s Radio Dongle, správný postup lze dohledat na webu výrobce https://www.bigclown.com/cs/ </li>
	<li>V Debug monitoru v NODE-red je nopřeba dohledat detekovaný název modůlu a upravit tento název v daném bloku, tuto úpravu je nutné provést i ve všech 3 blocích pro funkce, zde je to v proměnné "msg.topic"</li>
	<li>Pokud je vše správně nastavené už by mělo vše být plně funkční</li>
</ol>
